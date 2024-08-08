# MedusaApp

MedusaApp is a full-stack e-commerce application built with Medusa, featuring both frontend and backend components.

## Project Structure

- `backend/`: Contains the Medusa backend application
- `storefront/`: Contains the Medusa storefront application (Next.js)
- `docker-compose.yml`: Docker configuration for the project

## Prerequisites

- Node.js version 14 or later
- Docker and Docker Compose
- Yarn package manager

## Getting Started

1. **Start Docker:**
   Ensure Docker is running on your machine before proceeding.

2. **Install dependencies:**
   Open a terminal and run the following commands:

   ```bash
   # Install backend dependencies
   cd backend
   yarn install

   # Install storefront dependencies
   cd ../storefront
   yarn install
   ```

3. **Set up environment variables:**
   Create `.env` files in both `backend/` and `storefront/` directories with the necessary environment variables.

4. **Start the application:**
   From the root directory of the project, run:

   ```bash
   docker-compose up
   ```

   This will start the required services (PostgreSQL, Redis, etc.).

5. **Start the backend and storefront:**
   In separate terminal windows, run:

   For the backend:

   ```bash
   cd backend
   yarn dev
   ```

   For the storefront:

   ```bash
   cd storefront
   yarn dev
   ```

Now your Medusa backend should be running on `http://localhost:9000` and the storefront on `http://localhost:3000`.

## Features

- Product management
- Order processing
- Customer accounts
- Shopping cart functionality
- Checkout process
- [Add any specific features of your implementation]

## API Documentation

The Medusa backend provides a RESTful API. You can access the API documentation at `http://localhost:9000/store/docs` when your backend server is running.

## Customization

### Backend

To add custom endpoints or services:

1. Create new files in the `src/api` directory for API routes.
2. Add services in the `src/services` directory.
3. Use the `src/subscribers` directory for event subscribers.

### Storefront

The storefront is built with Next.js. Customize the UI by modifying the components in the `src/components` directory and pages in the `src/pages` directory.

## Resources

- [Medusa Documentation](https://docs.medusajs.com/)
- [Medusa GitHub Repository](https://github.com/medusajs/medusa)
- [Next.js Documentation](https://nextjs.org/docs)
