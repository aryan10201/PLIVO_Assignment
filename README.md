# Status Page Application

A modern status page application built with Next.js and Express.js that allows you to monitor and report the status of your services and components.

## Features

- Real-time status monitoring
- Incident management
- Component status tracking
- User authentication
- Responsive design
- Uptime charts
- Role-based access control

## Tech Stack

- **Frontend**: Next.js, React, Tailwind CSS
- **Backend**: Express.js, Node.js
- **Database**: MongoDB
- **Authentication**: JWT
- **Deployment**: Vercel

## Prerequisites

- Node.js (v14 or higher)
- MongoDB (local or Atlas)
- npm or yarn

## Project Structure

```
.
├── Frontend/                 # Next.js frontend application
│   ├── components/          # React components
│   ├── pages/              # Next.js pages
│   ├── lib/                # Utility functions and configurations
│   └── public/             # Static assets
└── Backend/                # Express.js backend application
    ├── models/             # MongoDB models
    ├── routes/             # API routes
    └── server.js           # Express server
```

## Environment Configuration

### Frontend (.env.local)

```env
API_URL=http://localhost:5001
MONGODB_URI=mongodb://localhost:27017/status-page
MONGODB_DB=status-page
JWT_SECRET=your-secret-key-here
```

### Backend (.env)

```env
PORT=5001
MONGODB_URI=mongodb://localhost:27017/status-page
JWT_SECRET=your-secret-key-here
NODE_ENV=development
```

## Development Setup

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd status-page
   ```

2. Install dependencies:
   ```bash
   # Install frontend dependencies
   cd Frontend
   npm install

   # Install backend dependencies
   cd ../Backend
   npm install
   ```

3. Set up environment variables:
   - Create `.env.local` in the Frontend directory
   - Create `.env` in the Backend directory
   - Copy the environment variables from the examples above

4. Start the development servers:
   ```bash
   # Start backend server
   cd Backend
   npm run dev

   # Start frontend server (in a new terminal)
   cd Frontend
   npm run dev
   ```

5. Access the application:
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:5001

## API Documentation

### Components API

- `GET /api/components` - Get all components
- `POST /api/components` - Create a new component
- `PUT /api/components/:id` - Update a component
- `DELETE /api/components/:id` - Delete a component

### Incidents API

- `GET /api/incidents` - Get all incidents
- `POST /api/incidents` - Create a new incident
- `PUT /api/incidents/:id` - Update an incident
- `DELETE /api/incidents/:id` - Delete an incident

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request
