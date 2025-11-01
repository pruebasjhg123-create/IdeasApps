# Professional Cursor Prompt - Copy & Paste to Cursor Agent

## Instructions for Use

Copy the entire prompt below (starting from "## PROJECT BRIEF" section) and paste it into Cursor's Agent input field.

---

## PROJECT BRIEF

I need you to architect and develop a complete full-stack SaaS application called "Ideas Browser" following professional development standards.

### Phase 1: Foundation & Infrastructure

Start by establishing the core foundation:

**1. Project Structure Setup**
- Create complete directory structure as defined in .cursorrules
- Generate package.json with all required dependencies (Next.js, Express, MongoDB, TypeScript, testing libraries)
- Create .env.example with all required environment variables
- Setup docker-compose.yml for local development environment

**2. Backend Foundation (Express + TypeScript)**
- Initialize Express server with TypeScript configuration
- Implement middleware (CORS, error handling, logging, rate limiting)
- Create database connection setup (MongoDB with Mongoose)
- Implement JWT authentication system with token refresh logic
- Setup custom error handling and logging system
- Create API versioning structure (v1)

**3. Database Schema Design**
- Design and implement User schema (email, password, profile, preferences)
- Create Idea schema (title, description, source, metrics, analysis, tags, userId, timestamps)
- Design Integration schema (redditAuth, youtubeAuth, twitterAuth, lastSync)
- Implement proper indexing for performance
- Add validation rules and middleware

**4. Authentication System**
- Implement JWT token generation and validation
- Create secure password hashing with bcrypt
- Setup refresh token mechanism
- Create authentication middleware for protected routes
- Implement logout functionality

### Phase 2: API Endpoints Development

**Authentication Routes (/api/v1/auth)**
- POST /register - User registration with validation
- POST /login - User login returning JWT
- POST /refresh - Refresh access token
- POST /logout - Invalidate tokens
- GET /profile - Get authenticated user profile

**Ideas Routes (/api/v1/ideas)**
- GET /ideas - List ideas with filtering (by source, date, tag, keyword)
- POST /ideas - Create new idea (manual entry)
- GET /ideas/:id - Get idea details
- PUT /ideas/:id - Update idea
- DELETE /ideas/:id - Delete idea
- POST /ideas/:id/bookmark - Bookmark/save idea

**Analytics Routes (/api/v1/analytics)**
- GET /trends - Get trending ideas
- GET /statistics - Get user statistics
- GET /insights - Get AI-generated insights

**Integrations Routes (/api/v1/integrations)**
- GET /reddit/status - Check Reddit integration status
- POST /reddit/authorize - OAuth authorization flow
- GET /reddit/sync - Sync Reddit data
- GET /youtube/status - Check YouTube status
- POST /youtube/authorize - OAuth authorization
- GET /youtube/sync - Sync YouTube data

### Phase 3: Frontend Architecture (Next.js)

**Project Setup**
- Initialize Next.js 15 with App Router
- Configure TypeScript with strict mode
- Setup Tailwind CSS with custom theme
- Install shadcn/ui components
- Setup ESLint and Prettier

**Core Components Library**
- Create reusable UI components (Button, Card, Input, Modal, Toast, etc.)
- Implement Layout components (Header, Sidebar, Footer)
- Create Form components with validation
- Setup error boundary and error handling

**Pages & Views**
- Landing Page: Professional hero section, features, CTA
- Auth Pages: Login, Register, Password reset
- Dashboard: Main trends, quick stats, latest ideas
- Ideas Explorer: Advanced filtering, search, sorting
- User Profile: Settings, preferences, bookmarks
- Integration Settings: Connect Reddit, YouTube, Twitter

**State Management**
- Setup React hooks for state management
- Create API client with axios/fetch
- Implement proper error and loading states
- Add toast notifications system

### Phase 4: Documentation & Configuration

**Documentation Files**
- API.md: Complete API documentation with examples
- SETUP.md: Setup and installation instructions
- ARCHITECTURE.md: Technical architecture overview
- UPDATE README.md: Project overview, features, tech stack

**Configuration Files**
- tsconfig.json: Strict TypeScript configuration
- eslint.config.js: Code quality rules
- prettier.config.js: Code formatting
- .gitignore: Proper Git ignore rules

## TECHNICAL REQUIREMENTS

**Code Quality Standards**
- Write clean, maintainable TypeScript code
- Include comprehensive inline comments for complex logic
- Follow consistent naming conventions
- Implement proper error handling throughout
- Use meaningful variable and function names

**Security Requirements**
- Hash passwords with bcrypt
- Implement JWT token-based authentication
- Add CSRF protection
- Validate and sanitize all inputs
- Use environment variables for secrets
- Implement rate limiting

**Performance Requirements**
- Optimize database queries with proper indexing
- Implement caching strategies
- Use pagination for list endpoints
- Compress responses
- Optimize bundle size

**Development Standards**
- Create .env.example files for configuration
- Never hardcode secrets or API keys
- Write unit tests for business logic
- Document all API endpoints
- Use meaningful commit messages

## IMPLEMENTATION ORDER

1. Start with database schemas and types
2. Build backend authentication system
3. Create API endpoints with validation
4. Setup frontend project structure
5. Build authentication pages
6. Create dashboard and main pages
7. Implement API integration
8. Add error handling and loading states
9. Write documentation
10. Setup Docker configuration

## LANGUAGE & LOCALIZATION

- UI text and labels: **Spanish**
- Code comments: **English**
- Documentation: **English**
- Future: Prepare for bilingual support

## DELIVERABLES

This implementation should result in a complete, production-ready codebase including:
- Working backend API with authentication
- Functional frontend with all core pages
- Database schemas and connections
- Docker setup for local development
- Comprehensive documentation
- Error handling and validation
- Professional code organization

---

**Note**: Review the .cursorrules file for additional development guidelines and standards.
