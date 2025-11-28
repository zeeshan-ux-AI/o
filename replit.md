# Portfolio Website - Zeeshan

## Overview

This is a personal portfolio website for Zeeshan, a No-Code Web Developer and AI Builder from Bangladesh. The site showcases skills, projects, services, and contact information in a modern, responsive single-page application. Built with React and TypeScript, the portfolio emphasizes AI-powered development tools and no-code expertise.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture

**Framework Choice: React with TypeScript**
- The application uses React 18+ with TypeScript for type safety and modern component development
- Single Page Application (SPA) architecture using Wouter for lightweight client-side routing
- Component-based architecture with clear separation of concerns between UI components, pages, and utilities

**UI Framework: Shadcn/ui + Radix UI**
- Uses Shadcn/ui component library built on top of Radix UI primitives for accessible, customizable components
- Tailwind CSS for utility-first styling with custom design tokens
- Support for light/dark theme switching via ThemeProvider context
- Custom CSS variables for theming (colors, shadows, borders, fonts)

**State Management**
- React Query (@tanstack/react-query) for server state management and data fetching
- React Context API for theme management (ThemeProvider)
- Local component state using React hooks (useState, useEffect)

**Styling Architecture**
- Tailwind CSS with custom configuration for design system
- CSS custom properties for theme variables (light/dark mode)
- Class-variance-authority (CVA) for variant-based component styling
- Utility classes for elevation, hover effects, and transitions

**Project Structure**
- `/client/src/components` - Reusable UI components and page sections
- `/client/src/components/ui` - Shadcn/ui component library
- `/client/src/pages` - Page-level components (Home, NotFound)
- `/client/src/lib` - Utility functions and query client setup
- `/client/src/hooks` - Custom React hooks

### Backend Architecture

**Server Framework: Express.js (Implied)**
- The project structure suggests an Express.js backend (indicated by package name "rest-express")
- Server entry point at `server/index.ts` with development and production modes
- Session management using connect-pg-simple for PostgreSQL session storage

**Build System**
- Vite for frontend bundling and development server
- Custom build script (`script/build.ts`) for production builds
- TypeScript compilation with path aliases for clean imports
- Separate development and production environments

### Data Storage Solutions

**Database: PostgreSQL with Neon**
- Uses @neondatabase/serverless for serverless PostgreSQL connectivity
- Drizzle ORM for type-safe database queries and schema management
- Drizzle-kit for database migrations and schema pushing
- Connect-pg-simple for PostgreSQL-backed session storage

**Schema Management**
- Drizzle ORM provides type-safe schema definitions
- Schema validation using drizzle-zod for runtime type checking
- Database push command available via `npm run db:push`

### Authentication and Authorization

**Session-Based Authentication**
- PostgreSQL-backed sessions using connect-pg-simple
- Cookie-based session management with credentials: "include" for API requests
- Unauthorized request handling with configurable behavior (return null or throw)

### External Dependencies

**Third-Party UI Libraries**
- Radix UI - Accessible component primitives (@radix-ui/react-*)
- Shadcn/ui - Component library built on Radix
- Lucide React - Icon library
- React Icons - Additional icon library (specifically react-icons/si for brand icons)
- Embla Carousel - Carousel/slider functionality
- CMDK - Command menu component
- Vaul - Drawer component library

**Development Tools**
- React Hook Form with Zod resolvers for form validation
- Date-fns for date manipulation
- Wouter for lightweight routing
- Vite plugins for Replit integration (@replit/vite-plugin-*)

**Hosting and Deployment**
- Vercel configuration for deployment
- Static site generation with Vite build output to `dist/public`
- Rewrites configured for SPA routing

**Fonts**
- Google Fonts: Inter, JetBrains Mono, Space Grotesk
- Custom font variables defined in CSS

**Database Service**
- Neon serverless PostgreSQL for cloud database hosting
- WebSocket-compatible serverless driver for edge compatibility

**Key Architectural Decisions**
1. **SPA over SSR**: Chose client-side rendering for simplicity and static hosting compatibility
2. **Drizzle over Prisma**: Lightweight ORM with better TypeScript integration and edge runtime support
3. **Wouter over React Router**: Minimal routing library to reduce bundle size for simple navigation needs
4. **Shadcn/ui approach**: Copy-paste components rather than npm package for full customization control
5. **Neon serverless**: Serverless PostgreSQL allows for cost-effective scaling and edge deployment
6. **Session-based auth**: Traditional session cookies over JWT for simpler security model and built-in CSRF protection