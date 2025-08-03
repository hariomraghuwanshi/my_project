# GeoData Dashboard

## Overview

This is a React-based geospatial visualization dashboard that allows users to interact with time-series data overlaid on interactive maps. The application combines temporal navigation through a timeline slider with spatial data visualization through polygon creation and color-coded data display. Users can create custom regions on the map, apply data sources with configurable color rules, and navigate through time to observe data changes.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React with TypeScript using Vite as the build tool
- **UI Components**: shadcn/ui component library built on Radix UI primitives
- **Styling**: Tailwind CSS with CSS variables for theming
- **State Management**: Zustand for global application state
- **Data Fetching**: TanStack Query for server state management
- **Routing**: Wouter for lightweight client-side routing

### Component Structure
- **Dashboard Layout**: Split between collapsible sidebar and main content area
- **Timeline Slider**: Horizontal time navigation with play/pause functionality
- **Interactive Map**: Leaflet-based mapping with polygon drawing capabilities
- **Data Source Manager**: Configuration interface for external data sources and color rules
- **Polygon Manager**: Interface for managing created spatial regions

### Data Architecture
- **Data Sources**: Configurable external APIs with field mapping and color rule definitions
- **Weather Data Integration**: Open-Meteo API for historical weather data
- **Color Mapping**: Rule-based system for applying colors based on data thresholds
- **Temporal Navigation**: 30-day sliding window (15 days before/after current date)

### Map Features
- **Interactive Drawing**: Click-based polygon creation with real-time preview
- **Fixed Zoom Level**: Locked at 2 sq. km resolution as per requirements
- **Dynamic Coloring**: Polygons colored based on current data values and rules
- **Centroid Calculation**: Automatic polygon center calculation for data sampling

### State Management Design
- **Dashboard Store**: Centralized state for time range, map settings, polygons, and data sources
- **Real-time Updates**: Automatic data fetching when time range or polygons change
- **Drawing State**: Dedicated state management for polygon creation workflow

## External Dependencies

### Core Libraries
- **@tanstack/react-query**: Server state management and caching
- **react-leaflet**: React components for Leaflet mapping
- **leaflet**: Core mapping library for interactive maps
- **zustand**: Lightweight state management
- **wouter**: Minimal routing solution

### UI Framework
- **@radix-ui/***: Comprehensive set of accessible UI primitives
- **tailwindcss**: Utility-first CSS framework
- **class-variance-authority**: Component variant management
- **clsx**: Conditional className utility

### Data Integration
- **Open-Meteo API**: Historical weather data source
- **date-fns**: Date manipulation and formatting utilities
- **drizzle-orm**: Database ORM (configured for PostgreSQL)
- **@neondatabase/serverless**: Serverless PostgreSQL client

### Development Tools
- **vite**: Fast build tool and dev server
- **typescript**: Type safety and development experience
- **@replit/vite-plugin-***: Replit-specific development plugins

### Backend Infrastructure
- **Express.js**: Web server framework
- **PostgreSQL**: Database (via Drizzle configuration)
- **Node.js**: Runtime environment

The application follows a modern React architecture with clear separation of concerns, utilizing industry-standard libraries for mapping, state management, and UI components while maintaining type safety throughout the codebase.