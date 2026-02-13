# Full-Stack Web Application

This repository contains a full-stack web application built with Node.js,
Express, and SQLite. It includes scripts and documentation for setting up,
configuring, and deploying the application on an AWS EC2 instance.

- [Development Guide](dev-node/README.md)
- [Deployment Guide (Docker)](deploy-docker/README.md)
- [Deployment Guide (Manual)](deploy-node/README.md)

## Technology Stack
- Backend technology stack
    - Web Server: Django development server for local development. Production deployment configured for WSGI compatible servers such as Gunicorn behind a reverse proxy if deployed to cloud infrastructure.
    - Backend Runtime: Python 3.x
    - Backend Framework: Django
    - Database: SQLite for lightweight development and testing data storage
    - Routing and MVC Structure: Django built in URL routing and Model View Template architecture
    - Logging and Debugging: Django debug logging, structured console output, and VS Code debugger

Frontend technology stack
- Templates: Django Templates for server side rendering
    - UX and UI Framework: Bootstrap for responsive layout and styling
    - Static Asset Management: Django static file configuration

- Testing and Quality Assurance
    - Unit and Integration Testing: Django Test Runner
    - Test Execution: python manage.py test
    - Debug Verification: Console debug messages implemented in views to confirm route execution
    - Continuous Integration: GitHub Actions configured to execute automated tests on every commit

- Development Environment
IDE: VS Code and GitHub Codespaces
Version Control: Git with GitHub repository hosting

## Team Workflow
- Branching Strategy
    - Main branch contains stable and tested code
    - Feature branches are created for new functionality or bug fixes
    - Changes are merged into main only after validation

- Development Process
    - Developers implement features locally using Django development server
    - Unit tests are written or updated alongside feature development
    - Debug logging is used during development to verify route and view execution
    - Code is committed with descriptive commit messages

- Code Review and Validation
    - Pull requests are created before merging into main
    - Automated GitHub Actions workflow runs the full test suite on every push and pull request
    - Code must pass all tests before being approved for merge

- Testing Policy
    - Every route and core logic component must include test coverage
    - Tests must pass locally before pushing to repository
    - Debug output is used to verify correct runtime behavior

- Deployment Process
    - Application is verified locally prior to deployment
    - Deployment follows documented configuration steps
    - Production configuration removes debug mode and enforces secure settings
    
- Issue Tracking and Documentation
    - GitHub Issues used for tracking enhancements and bugs
    - README documentation updated as features evolve
    - Clear documentation ensures reproducibility of setup and deployment