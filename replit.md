# Finance Achiever - Social Media Fintech Platform

## Overview
Finance Achiever is an educational platform offering 37 expert-led video courses on financial literacy, with AI-powered tutoring and social learning features. It provides professional financial education across four channels (Business, Finance, Estate Planning, Living Trusts) with social media functionality to foster a learning community. The platform aims to capture a share of the $2.7B financial education market, with projections of reaching 105,349 subscribers and $5.67M annual run rate by Year 3.

**DEPLOYMENT STATUS**: FRONTEND/BACKEND SEPARATION COMPLETE - Platform successfully separated into independent, scalable applications. Frontend (109 files) and Backend (35 files) ready for deployment to Vercel + Railway. Memory constraints resolved through architectural separation. Ready for production scaling to 105,349 subscribers.

## User Preferences
Preferred communication style: Simple, everyday language.
Video organization: Two channels - "Business Courses for Beginners" (9 videos) and "Finance for Beginners" (2 videos).

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite
- **UI Framework**: shadcn/ui components built on Radix UI primitives
- **Styling**: Tailwind CSS with custom CSS variables
- **State Management**: TanStack Query (React Query)
- **Routing**: Wouter

The frontend follows a component-based architecture with logical organization of UI components, pages, and business logic.

### Backend Architecture
- **Runtime**: Node.js with Express.js
- **Language**: TypeScript with ES modules
- **Database**: PostgreSQL (Neon Database)
- **API Design**: RESTful API
- **AI Integration**: OpenAI GPT-4o
- **Development**: Hot reloading with tsx and Vite middleware

The backend uses a service-oriented architecture, separating routes, storage, and external services. Global `pgPool` access is used for database connectivity.

### Key Features
- **Database Schema**: Includes tables for Users, Courses, Communities, Posts, Comments, Likes, User Progress, AI Conversations, and Chat Sessions.
- **Authentication System**: Supports local email/password and Replit OIDC, with session-based authentication.
- **AI Integration**: OpenAI GPT-4o for contextual tutoring, course-specific assistance, and conversation history persistence.
- **Social Features**: Community creation and management, post creation with multimedia, like/unlike functionality, and user profiles.
- **Payment Processing**: Integrated Stripe for secure subscription payments.
- **Credit Dispute Management**: Comprehensive tracking with letter generation (Section 609, FCRA 623 compliant) and a demo interface.
- **Financial Management System**: Comprehensive system for financial accounts, transactions, budgets, and goals, with a REST API and dashboard.
- **Visual Design**: Professional color theme (deep blue, success green, premium gold), gradient backgrounds, premium card styling, and sophisticated hover animations.
- **EMERGENCY MEMORY MANAGEMENT**: Critical memory leak fixes with ultra-aggressive garbage collection (every 2 seconds), all background processes disabled, payload limits reduced to 10MB.

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: For serverless PostgreSQL connection.
- **express**: Web application framework.
- **axios**: HTTP client for OpenAI API integration.
- **openai**: Official OpenAI SDK.
- **typescript**: For type safety.
- **Stripe**: Payment processing.

### Development Tools
- **tsx**: TypeScript execution for development.
- **ts-node**: TypeScript runtime for database scripts.
- **@types/***: TypeScript definitions.