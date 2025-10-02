# PDF Text Extractor - Replit Project Setup

## Overview
This is a full-stack React/TypeScript application that provides advanced PDF text extraction capabilities with interactive highlighting, OCR support, and AI-powered processing. The app uses Vite as the build tool with an Express backend and is fully configured for the Replit environment. This project has been successfully imported from GitHub and configured for Replit.

## Recent Changes (2025-10-02)
- ✅ Successfully imported fresh GitHub clone into Replit environment
- ✅ Installed all npm dependencies (640 packages)
- ✅ Created PostgreSQL database for the application
- ✅ Ran database migrations (db:push) to create all tables
- ✅ Set up "Server" workflow running `npm run dev:full` on port 5000
- ✅ Configured VM deployment with build and start scripts
- ✅ Verified application works with PDF upload interface
- ✅ Frontend properly configured with allowedHosts: true for Replit proxy
- ✅ Added API key input fields for Gemini and OpenAI integration
- ✅ Updated Gemini service to accept user-provided API keys with fallback to environment variables
- ✅ Fully integrated API keys through component hierarchy (PDFViewer → EnhancedPDFProcessor → geminiService)
- ✅ All systems operational (API keys optional, user-provided)

## Project Architecture
- **Frontend**: React 18 + TypeScript + Vite
- **Backend**: Express 5.x server with API routes
- **Database**: PostgreSQL with Drizzle ORM
- **UI Framework**: shadcn/ui + Tailwind CSS
- **Routing**: React Router DOM
- **State Management**: TanStack Query for server state
- **PDF Processing**: react-pdf + pdf-parse-fork + tesseract.js for OCR
- **AI Integration**: OpenAI & Google Gemini support
- **Build Tool**: Vite 5.x + esbuild for server

## Key Features
- PDF document upload and processing
- Text extraction with bounding box visualization
- OCR support for scanned documents
- Interactive text highlighting
- Search functionality across extracted text
- Multi-page document support
- Responsive design with dark mode support

## Configuration Files
- `vite.config.ts`: Development server configured for Replit (port 5000, host 0.0.0.0)
- `tailwind.config.ts`: Custom PDF viewer design system colors
- `package.json`: Added production start script for deployment
- `index.html`: SEO optimized with meta tags

## Development Workflow
1. Run `npm run dev:full` to start full-stack server on port 5000
   - Express server handles API routes and serves Vite dev server
   - Frontend automatically reloads on file changes via HMR
   - Backend API available at `/api/*` endpoints
2. Database migrations: `npm run db:push` (or `npm run db:push --force`)
3. Build for production with `npm run build:full`

## Deployment Configuration
- Target: VM (always-on server for stateful application)
- Build: `npm run build:full` (builds both frontend and backend)
- Run: `npm run start:full` (runs production Express server on port 5000)
- Note: Users will need to provide their own OpenAI/Gemini API keys

## Dependencies Highlights
- Core: React, TypeScript, Vite
- UI: shadcn/ui components, Tailwind CSS, Lucide React icons
- PDF: react-pdf, tesseract.js for OCR
- Routing: React Router DOM
- State: TanStack Query
- Forms: React Hook Form + Zod validation

## User Preferences
- Clean, modern UI with interactive PDF processing capabilities
- Responsive design optimized for both desktop and mobile
- Professional color scheme with proper contrast