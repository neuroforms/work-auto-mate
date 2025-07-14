# OptiFlow - AI Agent Platform

## Overview

OptiFlow is a web-based AI agent platform that enables users to create, execute, and manage automated workflows through natural language commands. The application combines AI-powered task planning with web automation capabilities, allowing users to automate complex workflows involving data extraction, file processing, and browser interactions.

## User Preferences

Preferred communication style: Simple, everyday language.

## Recent Changes

**January 14, 2025:**
✓ Successfully implemented complete OptiFlow AI Agent Platform
✓ Configured OpenAI API integration for task planning and file analysis
✓ Built comprehensive dashboard with real-time features
✓ Fixed TypeScript compilation errors
✓ Database schema deployed and ready
✓ Authentication system working with Replit Auth
✓ WebSocket connections established for real-time updates
✓ All core modules operational: Command Input, Task Planning, File Analysis, Workflow Builder, Task Scheduler, Execution Logs

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Styling**: Tailwind CSS with shadcn/ui component library
- **State Management**: TanStack React Query for server state management
- **Routing**: Wouter for lightweight client-side routing
- **Build Tool**: Vite for fast development and optimized builds

### Backend Architecture
- **Framework**: Express.js with TypeScript
- **Runtime**: Node.js with ES modules
- **API Design**: RESTful API with WebSocket support for real-time updates
- **Authentication**: Replit Auth integration with session-based authentication
- **File Processing**: Multer for file uploads with AI-powered analysis

### Database Layer
- **ORM**: Drizzle ORM for type-safe database operations
- **Database**: PostgreSQL (configured for Neon serverless)
- **Migrations**: Drizzle Kit for schema management
- **Session Storage**: PostgreSQL-based session store

## Key Components

### AI Integration
- **LLM Provider**: OpenAI GPT-4o for task planning and natural language processing
- **Task Planning**: Converts user commands into structured, executable workflows
- **File Analysis**: AI-powered document and data extraction

### Automation Engine
- **Web Automation**: Puppeteer for headless browser automation
- **Task Execution**: Queue-based system for managing and executing workflows
- **Real-time Updates**: WebSocket connections for live progress tracking

### User Interface Components
- **Command Input**: Natural language and voice command interface
- **Task Planner**: Visual workflow representation and editing
- **File Analyzer**: Upload and AI-powered file processing
- **Workflow Builder**: Drag-and-drop workflow creation interface
- **Task Scheduler**: Automated task scheduling and management
- **Execution Log**: Real-time task execution monitoring

### Data Models
- **Users**: Authentication and profile management
- **Workflows**: Reusable automation templates
- **Tasks**: Individual execution instances
- **Files**: Uploaded documents and analysis results
- **Execution Logs**: Detailed task execution history

## Data Flow

1. **User Input**: Commands entered via text or voice interface
2. **AI Processing**: OpenAI API converts commands to structured task plans
3. **Task Creation**: Structured plans stored in database as executable tasks
4. **Execution Engine**: Puppeteer and other services execute automation steps
5. **Progress Tracking**: WebSocket connections provide real-time updates
6. **Results Storage**: Execution results and logs stored for user access

## External Dependencies

### Core Services
- **OpenAI API**: GPT-4o for natural language processing and task planning
- **Neon Database**: Serverless PostgreSQL hosting
- **Replit Auth**: Authentication and user management

### Development Tools
- **shadcn/ui**: Pre-built accessible UI components
- **Radix UI**: Headless UI primitives for custom components
- **Lucide React**: Icon library for consistent iconography

### Automation Libraries
- **Puppeteer**: Web browser automation and scraping
- **Multer**: File upload handling middleware
- **ws**: WebSocket library for real-time communication

## Deployment Strategy

### Development Environment
- **Local Development**: Vite dev server with hot module replacement
- **Backend**: tsx for TypeScript execution with auto-reload
- **Database**: Neon serverless PostgreSQL connection

### Production Build
- **Frontend**: Vite build with static asset optimization
- **Backend**: esbuild bundling for Node.js deployment
- **Assets**: Static files served from dist/public directory

### Environment Configuration
- **Database**: DATABASE_URL for PostgreSQL connection
- **Authentication**: REPLIT_DOMAINS and SESSION_SECRET for auth
- **AI Services**: OPENAI_API_KEY for GPT integration
- **Development**: NODE_ENV for environment-specific behavior

### Session Management
- **Storage**: PostgreSQL-based session store with configurable TTL
- **Security**: HTTP-only cookies with secure flag in production
- **Persistence**: 7-day session lifetime with automatic cleanup

The application is designed as a monorepo with clear separation between client, server, and shared code, enabling efficient development and deployment while maintaining type safety across the entire stack.