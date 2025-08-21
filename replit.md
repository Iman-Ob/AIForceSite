# Overview

This is a full-stack web application called AIFORCE that presents a military-themed AI services company. The application features a modern landing page showcasing AI products and services with tactical military branding. It includes functionality for displaying products, services, contact forms, and an admin section for content management. The app uses React with TypeScript on the frontend, Express.js on the backend, and is configured for PostgreSQL database with Drizzle ORM.

# User Preferences

Preferred communication style: Simple, everyday language.

# System Architecture

## Frontend Architecture
- **Framework**: React 18 with TypeScript and Vite for build tooling
- **UI Library**: Shadcn/ui components built on Radix UI primitives with Tailwind CSS for styling
- **State Management**: React Query (TanStack Query) for server state management and caching
- **Routing**: Wouter for lightweight client-side routing
- **Form Handling**: React Hook Form with Zod validation for type-safe form validation
- **Styling**: Tailwind CSS with custom tactical/military theme colors and responsive design

## Backend Architecture
- **Framework**: Express.js with TypeScript running on Node.js
- **API Design**: RESTful API with endpoints for products, services, and contacts
- **Request Handling**: Express middleware for JSON parsing, URL encoding, and request logging
- **Error Handling**: Centralized error handling middleware with proper HTTP status codes
- **Development**: Hot reloading with Vite integration for seamless development experience

## Database Architecture
- **ORM**: Drizzle ORM configured for PostgreSQL with schema-first approach
- **Database**: PostgreSQL using Neon Database serverless driver (@neondatabase/serverless)
- **Schema Management**: Drizzle Kit for migrations with schema defined in shared/schema.ts
- **Data Models**: Three main entities - Products (with status tracking), Services (with pricing), and Contacts (for lead capture)
- **Validation**: Zod schemas for runtime type checking and validation

## Project Structure
- **Monorepo Layout**: Shared TypeScript configuration and dependencies
- **Client Directory**: React frontend application with component-based architecture
- **Server Directory**: Express.js backend with modular route handling
- **Shared Directory**: Common schemas and types used by both frontend and backend
- **Component Organization**: UI components in shadcn/ui structure with custom business components

## Development & Build
- **Build System**: Vite for frontend bundling with esbuild for backend compilation
- **Development**: Concurrent development server with hot module replacement
- **TypeScript**: Strict type checking with path mapping for clean imports
- **Environment**: Development/production environment configuration with Replit integration

## Cloud Storage Integration
- **File Storage**: Google Cloud Storage integration with @google-cloud/storage
- **File Upload**: Uppy.js integration for file handling with AWS S3 and drag-drop support
- **Asset Management**: Configured asset paths for attached assets and static files

# External Dependencies

## Core Technologies
- **Database**: PostgreSQL via Neon Database serverless platform
- **Cloud Storage**: Google Cloud Storage for file and asset management
- **CDN**: Google Fonts for typography (Inter, DM Sans, Fira Code, Geist Mono, Architects Daughter)

## Third-party Libraries
- **UI Framework**: Radix UI primitives for accessible component foundation
- **File Upload**: Uppy.js ecosystem for file handling and upload workflows
- **Validation**: Zod for schema validation and type safety
- **State Management**: TanStack Query for server state caching and synchronization
- **Form Management**: React Hook Form for performant form handling

## Development Tools
- **Build Tools**: Vite with TypeScript support and React plugin
- **Code Quality**: ESLint configuration and TypeScript strict mode
- **Styling**: Tailwind CSS with PostCSS and Autoprefixer
- **Development**: Replit-specific plugins for enhanced development experience

## Hosting & Deployment
- **Platform**: Configured for Replit deployment with development banner integration
- **Environment Variables**: DATABASE_URL for PostgreSQL connection string
- **Static Assets**: Vite-based static file serving with proper asset resolution