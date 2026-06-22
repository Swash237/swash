# Management System

A comprehensive project and task management system built with Node.js, Express, React, and PostgreSQL.

## Features

- **User Management**: Create, update, and manage user accounts
- **Project Management**: Organize projects with teams and workflows
- **Task Tracking**: Create, assign, and track tasks with status updates
- **User Authentication**: Secure JWT-based authentication
- **Dashboard**: Real-time project overview and analytics
- **Reporting**: Generate reports on project progress
- **Role-Based Access Control**: Different permission levels for users

## Tech Stack

### Backend
- Node.js + Express.js
- PostgreSQL Database
- JWT Authentication
- RESTful API

### Frontend
- React 18
- Redux for State Management
- Material-UI Components
- Axios for API Calls

## Getting Started

### Prerequisites
- Node.js (v16+)
- PostgreSQL (v12+)
- npm or yarn

### Installation

1. Clone the repository
```bash
git clone <repo-url>
cd management-system
```

2. Install dependencies
```bash
npm install
cd client && npm install && cd ..
```

3. Set up environment variables
```bash
cp .env.example .env
# Edit .env with your configuration
```

4. Create and migrate the database
```bash
npm run db:migrate
npm run db:seed
```

5. Start the development server
```bash
# Terminal 1: Backend
npm run dev

# Terminal 2: Frontend
npm run client
```

The application will be available at `http://localhost:3000`

## Project Structure

```
management-system/
├── server/
│   ├── controllers/     # Request handlers
│   ├── models/         # Database models
│   ├── routes/         # API routes
│   ├── middleware/      # Express middleware
│   ├── utils/          # Utility functions
│   └── index.js        # Server entry point
├── client/
│   ├── src/
│   │   ├── components/ # React components
│   │   ├── pages/      # Page components
│   │   ├── redux/      # Redux store
│   │   ├── services/   # API services
│   │   └── App.js
│   └── package.json
├── database/
│   ├── migrations/     # Database migrations
│   └── seeds/          # Seed data
├── scripts/
│   ├── migrate.js      # Migration runner
│   └── seed.js         # Data seeder
└── .env.example
```

## API Endpoints

### Authentication
- `POST /api/auth/register` - Register new user
- `POST /api/auth/login` - Login user
- `POST /api/auth/logout` - Logout user

### Users
- `GET /api/users` - Get all users
- `GET /api/users/:id` - Get user by ID
- `PUT /api/users/:id` - Update user
- `DELETE /api/users/:id` - Delete user

### Projects
- `GET /api/projects` - Get all projects
- `POST /api/projects` - Create new project
- `GET /api/projects/:id` - Get project details
- `PUT /api/projects/:id` - Update project
- `DELETE /api/projects/:id` - Delete project

### Tasks
- `GET /api/tasks` - Get all tasks
- `POST /api/tasks` - Create new task
- `GET /api/tasks/:id` - Get task details
- `PUT /api/tasks/:id` - Update task
- `DELETE /api/tasks/:id` - Delete task
- `PUT /api/tasks/:id/assign` - Assign task to user

### Team Members
- `GET /api/teams/:projectId/members` - Get project members
- `POST /api/teams/:projectId/members` - Add member to project
- `DELETE /api/teams/:projectId/members/:userId` - Remove member

## Database Schema

See `database/schema.sql` for complete database schema including:
- Users table
- Projects table
- Tasks table
- Team Members table
- Activity logs

## Contributing

1. Create a feature branch (`git checkout -b feature/amazing-feature`)
2. Commit changes (`git commit -m 'Add amazing feature'`)
3. Push to branch (`git push origin feature/amazing-feature`)
4. Open a Pull Request

## License

MIT License - see LICENSE file for details
