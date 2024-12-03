# .github
---

# Guard Reports

Guard Reports is a guard management platform designed to streamline operations and improve reporting accuracy for security firms, property managers, and guards. The platform enhances lead generation and sales funnels for [OfficerMetrics](https://your-officermetrics-link.com), while also standing as a powerful independent solution for guard activity and incident management.

## Features

### Web Application
- **Client Management**: Track and manage client data effectively.
- **Guard Management**: Assign guards to tasks and manage their schedules.
- **Analytics & Reporting**: Generate actionable insights from activity and incident reports.

### Mobile Application
- **Guard Activity Logging**: Enable guards to log activities in real-time.
- **Incident Reporting**: Simplified forms for accurate and timely incident reports.
- **Cross-Platform Support**: Built with Expo to target both iOS and Android devices.

### API Server
- **Data Integration**: RESTful API to manage and sync data across the platform.
- **Performance-Optimized**: Built with NestJS for scalable and maintainable code.

## Tech Stack
- **Frontend**: React, React Native (using Expo)
- **Backend**: NestJS
- **Database**: PostgreSQL
- **Deployment**: Hosted on AWS (S3 for static assets, RDS for PostgreSQL, EC2/containers for the API and web app)
- **CICD**: Automated pipelines using GitHub Actions

## Architecture Overview
The platform consists of:
1. A **Web App** for administrative tasks and analytics.
2. A **Mobile App** for on-the-go guard activity reporting.
3. An **API Server** for centralized data management.

![Architecture Diagram Placeholder](path/to/architecture-diagram.png)

## Getting Started

### Prerequisites
- Node.js (v20+)
- PostgreSQL (v13+)
- AWS CLI configured for deployment

### Setup Instructions
1. Clone the repositories:
   - Web App: `https://github.com/your-org/guard-reports-web`
   - Mobile App: `https://github.com/your-org/guard-reports-mobile`
   - API Server: `https://github.com/your-org/guard-reports-api`

2. Install dependencies:
   ```bash
   cd guard-reports-web
   npm install
   # Repeat for mobile and API repos
   ```

3. Configure environment variables:
   - Refer to `.env.example` files in each repo for required configurations.

4. Set up the database:
   - Run migrations and seed initial data.
   ```bash
   cd guard-reports-api
   npm run migrations
   npm run seed
   ```

5. Run the apps:
   - Web App: `npm start` (http://localhost:3000)
   - Mobile App: `expo start`
   - API Server: `npm run start:dev`

### Deployment
- The platform is deployed to AWS:
  - **Web and API** hosted on EC2/containers.
  - **Static Assets** stored in S3.
  - **Database** managed in RDS.
- CICD pipelines for automated deployments are set up using GitHub Actions.

## Contributing

Please follow these steps to contribute:

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature-name`
3. Ensure code quality by following our linting and formatting standards:
   - **Prettier**: Formats the code for consistency.
   - **ESLint**: Enforces code style and identifies common issues.
   - Run the tools before committing:
     ```bash
     npm run lint   # Check for linting errors
     npm run format # Automatically format code
     ```

4. Commit your changes using the following best-practice template:
   ```
   [TYPE]: [Short Description]

   [Optional Detailed Description]
   
   [Ticket or Issue Number]
   ```

   #### Commit Message Types
   - **feat**: A new feature
   - **fix**: A bug fix
   - **docs**: Documentation updates
   - **style**: Code style changes (formatting, missing semi-colons, etc., not affecting functionality)
   - **refactor**: Code changes that neither fix a bug nor add a feature
   - **test**: Adding or updating tests
   - **chore**: Maintenance tasks (e.g., updating dependencies)

   #### Example Commit Messages
   - `feat: Add user authentication module`
   - `fix: Correct guard schedule validation logic`
   - `docs: Update README setup instructions`
   - `chore: Bump NestJS to version 9.0.0`

5. Push to your branch: `git push origin feature-name`
6. Submit a pull request.

### Prettier and ESLint Configuration
- **Prettier** and **ESLint** configurations are included in the repository.
- Pre-commit hooks are set up using `husky` to enforce these rules automatically. Ensure these hooks are active:
  ```bash
  npm install
  npm run prepare # Activates husky hooks
  ```
- Any commit that fails linting or formatting will be rejected until corrected.

---
