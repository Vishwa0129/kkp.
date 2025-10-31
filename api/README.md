# KKP Creative & Tech Solutions - Backend API

A robust, production-ready Node.js backend API built with Express, TypeScript, PostgreSQL, and Redis.

## Features

- 🚀 Express.js with TypeScript
- 🗄️ PostgreSQL database with connection pooling
- ⚡ Redis caching
- 🔒 Security middleware (Helmet, CORS, Rate Limiting)
- 📧 Email notifications (Nodemailer)
- 📝 Winston logging
- ✅ Input validation (express-validator)
- 🐳 Docker support
- 🧪 Ready for testing

## Getting Started

### Prerequisites

- Node.js 18+
- PostgreSQL 15+
- Redis 7+

### Installation

```bash
# Install dependencies
npm install

# Copy environment file
cp .env.example .env

# Edit .env with your configuration
```

### Development

```bash
# Run in development mode with hot reload
npm run dev

# Run in production mode
npm run build
npm start
```

### Database Setup

```bash
# Create database schema
psql -U kkp -d kkp_db -f src/database/schema.sql

# Or run migrations
npm run migrate
```

### Docker

```bash
# Build and run with Docker
docker-compose up --build

# Run in background
docker-compose up -d

# View logs
docker-compose logs -f api
```

## API Endpoints

### Health Check
- `GET /api/health` - Basic health check
- `GET /api/health/ready` - Readiness probe (checks database and Redis)

### Contact Form
- `POST /api/contact` - Submit contact form
- `GET /api/contact` - Get all contacts
- `GET /api/contact/:id` - Get contact by ID
- `PATCH /api/contact/:id/status` - Update contact status

### Projects
- `GET /api/projects` - Get all projects
- `GET /api/projects/featured` - Get featured projects
- `GET /api/projects/:id` - Get project by ID
- `GET /api/projects/category/:category` - Get projects by category

### Services
- `GET /api/services` - Get all services
- `GET /api/services/popular` - Get popular services
- `GET /api/services/:id` - Get service by ID
- `GET /api/services/category/:category` - Get services by category

## Environment Variables

See `.env.example` for all available configuration options.

## Testing

```bash
# Run tests
npm test

# Run with coverage
npm run test:coverage
```

## Logging

Logs are written to:
- Console (development)
- `logs/combined.log` (all logs)
- `logs/error.log` (errors only)
- `logs/exceptions.log` (uncaught exceptions)
- `logs/rejections.log` (unhandled rejections)

## License

Copyright © 2024 KKP Creative & Tech Solutions

