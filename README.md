# perekine-config

This repository contains configuration files used by `perekine-builder` during the build process.

## Purpose

Centralizes build configuration separate from the service code, allowing:
- Configuration changes without rebuilding
- Shared configuration across multiple services
- Version-controlled build settings
- Environment-specific configurations

## Configuration Files

### build-config.yml

Main build configuration file containing:
- Build parameters
- Environment settings
- Deployment configurations
- Feature flags

### environments/

Directory containing environment-specific configurations:
- `development.yml` - Development environment settings
- `staging.yml` - Staging environment settings  
- `production.yml` - Production environment settings

## Usage

The `perekine-builder` workflow automatically checks out this repository and reads configuration files during the build process. Configuration is read at build time, ensuring the latest settings are always used.

## Configuration Schema

See `build-config.yml` for the full configuration schema and available options.
