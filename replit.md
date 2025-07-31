# Tic-Tac-Toe Web Application

## Overview

This is a modern web-based Tic-Tac-Toe game built with a full-stack TypeScript architecture. The application features multiple game modes including human vs AI, human vs human, and AI vs AI gameplay, along with comprehensive game statistics tracking and session history.

## User Preferences

Preferred communication style: Simple, everyday language.
Owner branding: "izuuu" prominently displayed in header and footer.

## System Architecture

The application follows a monorepo structure with clear separation between client, server, and shared code:

- **Frontend**: React with TypeScript using Vite as the build tool
- **Backend**: Express.js server with TypeScript
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Styling**: Tailwind CSS with shadcn/ui component library
- **State Management**: TanStack Query for server state management

## Key Components

### Frontend Architecture
- **React 18** with TypeScript for the UI layer
- **Vite** for fast development and optimized builds
- **shadcn/ui** components built on Radix UI primitives for accessible, customizable UI
- **Tailwind CSS** for utility-first styling with CSS variables for theming
- **TanStack Query** for efficient server state management and caching
- **Wouter** for lightweight client-side routing
- **Framer Motion** for smooth animations in the game interface

### Backend Architecture
- **Express.js** server with TypeScript for API endpoints
- **Drizzle ORM** for type-safe database operations and migrations
- **PostgreSQL** database with full persistence for game data
- RESTful API design with proper error handling middleware
- Database-backed storage for game sessions, statistics, and user data

### Game Logic
- Multiple AI difficulty levels (easy, medium, hard) with different algorithms
- Minimax algorithm implementation for challenging AI opponents
- Support for three game modes: human vs AI, human vs human, AI vs AI
- Real-time game state management with move history tracking

### Database Schema
- **users**: User authentication and profile data
- **game_sessions**: Complete game history with moves, duration, and outcomes
- **game_stats**: Aggregated statistics for wins, losses, and draws
- All tables use UUID primary keys with proper relationships

## Data Flow

1. **Game Initialization**: User selects game mode and difficulty through the frontend
2. **Move Processing**: Moves are validated on the frontend and sent to the backend for persistence
3. **AI Processing**: AI moves are calculated using various algorithms based on difficulty
4. **State Synchronization**: Game state is kept in sync between client and server
5. **Statistics Updates**: Game completion triggers statistics updates in the database
6. **History Tracking**: All games are saved with complete move history for replay

## External Dependencies

### Core Framework Dependencies
- **React ecosystem**: React, React DOM, React Query for frontend functionality
- **Express.js**: Web server framework with middleware support
- **Drizzle**: Modern TypeScript ORM with PostgreSQL support

### UI and Styling
- **Radix UI**: Accessible, unstyled component primitives
- **Tailwind CSS**: Utility-first CSS framework
- **Lucide React**: Icon library for consistent iconography
- **Framer Motion**: Animation library for enhanced user experience

### Development Tools
- **Vite**: Fast build tool with HMR support
- **TypeScript**: Static typing for both frontend and backend
- **ESBuild**: Fast JavaScript bundler for production builds
- **Replit integration**: Custom plugins for development environment

## Deployment Strategy

### Development Environment
- **Vite dev server** for frontend development with hot module replacement
- **tsx** for running TypeScript server code directly
- **Concurrent development**: Frontend and backend run together in development mode

### Production Build
- **Frontend**: Vite builds optimized static assets to `dist/public`
- **Backend**: ESBuild bundles server code to `dist/index.js`
- **Database**: Drizzle handles schema migrations and database provisioning
- **Environment**: Configured for Node.js production deployment

### Database Management
- **Drizzle Kit** for schema migrations and database management
- **PostgreSQL** connection via environment variables
- **Migration system** for safe schema updates in production

The application is designed to be easily deployable on platforms like Replit, Vercel, or traditional Node.js hosting with minimal configuration changes.