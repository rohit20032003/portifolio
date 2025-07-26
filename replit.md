# Portfolio Application

## Overview

This is a modern full-stack portfolio application built with React, Express, and TypeScript. The application showcases a personal portfolio with sections for user information, education, skills, experience, projects, and contact functionality. It uses a component-based architecture with shadcn/ui for the frontend and Express.js for the backend API.

## User Preferences

Preferred communication style: Simple, everyday language.

## Content Management

The portfolio website is fully editable after deployment. All content including names, contact information, skills, experience, projects, and education can be easily updated through:
- Direct code editing in `server/storage.ts` for immediate changes
- API endpoints for programmatic updates
- File replacement for resume PDF and images

Key editable content areas:
- Personal information (name, email, phone, location)
- Professional details (tagline, mission, stats)
- Education and experience history
- Skills and proficiency levels
- Project information and descriptions
- Contact information and social links

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Styling**: Tailwind CSS with shadcn/ui component library
- **State Management**: TanStack Query (React Query) for server state
- **Routing**: Wouter for client-side routing
- **Build Tool**: Vite for development and production builds
- **Form Handling**: React Hook Form with Zod validation

### Backend Architecture
- **Framework**: Express.js with TypeScript
- **Runtime**: Node.js with ESM modules
- **API Pattern**: RESTful API design
- **Middleware**: Express middleware for JSON parsing and request logging

### Data Storage
- **ORM**: Drizzle ORM for database interactions
- **Database**: PostgreSQL (configured via Drizzle)
- **Schema**: Centralized schema definitions in shared directory
- **Fallback**: In-memory storage implementation for development

## Key Components

### Database Schema
- **Portfolios Table**: Stores user portfolio data as JSONB
- **Contacts Table**: Stores contact form submissions
- **Schema Validation**: Zod schemas for runtime type checking

### API Endpoints
- `GET /api/portfolio/:userId` - Retrieve portfolio data
- `PUT /api/portfolio/:userId` - Update portfolio data
- `POST /api/contact` - Submit contact form

### Frontend Components
- **Navigation**: Fixed navigation with smooth scrolling
- **Hero Section**: Main landing area with user introduction
- **About Section**: Personal information, values, and education
- **Skills Section**: Technical skills with proficiency levels
- **Experience Section**: Work experience and internships
- **Projects Section**: Featured and other projects
- **Contact Section**: Contact form and information

### UI Components
- **shadcn/ui**: Complete component library for consistent design
- **Responsive Design**: Mobile-first approach with Tailwind CSS
- **Dark Mode**: CSS variable-based theming system

## Data Flow

1. **Initial Load**: Frontend queries portfolio data via React Query
2. **Data Fetching**: Express API serves portfolio data from storage layer
3. **Form Submissions**: Contact forms submit data through API endpoints
4. **Real-time Updates**: React Query handles caching and background updates
5. **Error Handling**: Centralized error handling with toast notifications

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: Neon database connection
- **@tanstack/react-query**: Server state management
- **@hookform/resolvers**: Form validation integration
- **drizzle-orm**: Database ORM
- **wouter**: Lightweight routing

### UI Dependencies
- **@radix-ui**: Accessible UI primitives
- **tailwindcss**: Utility-first CSS framework
- **class-variance-authority**: Component variant management
- **lucide-react**: Icon library

### Development Dependencies
- **vite**: Build tool and dev server
- **typescript**: Type checking
- **tsx**: TypeScript execution
- **esbuild**: Production bundling

## Deployment Strategy

### Development
- **Dev Server**: Vite dev server with HMR for frontend
- **API Server**: Express server with tsx for TypeScript execution
- **Database**: Uses DATABASE_URL environment variable

### Production Build
1. **Frontend Build**: Vite builds React app to `dist/public`
2. **Backend Build**: esbuild bundles Express server to `dist/index.js`
3. **Static Serving**: Express serves built frontend files
4. **Database**: Drizzle migrations via `db:push` script

### Environment Configuration
- **Development**: NODE_ENV=development with hot reloading
- **Production**: NODE_ENV=production with optimized builds
- **Database**: PostgreSQL connection via DATABASE_URL
- **Replit Integration**: Special handling for Replit environment

### File Structure
- `client/` - React frontend application
- `server/` - Express backend application  
- `shared/` - Shared TypeScript schemas and types
- `dist/` - Production build output
- Configuration files in root directory

The application follows a monorepo structure with clear separation between frontend, backend, and shared code, making it maintainable and scalable.