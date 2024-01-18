# MOMO Payment Processor

Welcome to the MOMO Payment Processor project! This payment processor is designed to save payments, track their status, and provide a seamless payment experience for your clients.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

Our MOMO Payment Processor is built to meet the following requirements:

- Clients can save payments with relevant details such as amount, payment method, phone number, operator, and a unique reference.
- Clients can view their payment history.
- Payments should only be processed once.
- Integration with an external payment provider, [xyz.com](https://xyz.com), for status updates.
- Built with Node.js (TypeScript), NestJS, PostgresSQL, and Prisma.

## Features

- **Save Payments**: Clients can save payments with relevant details.
- **View Payment History**: Clients can easily access their payment history.
- **Integration**: Seamless integration with an external payment provider.
- **Data Integrity**: Ensures that payments are processed only once.
- **Data Persistence**: Utilizes PostgresSQL as the database for data storage.
- **TypeScript**: Written in TypeScript for type safety and better code quality.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- [Node.js](https://nodejs.org/) installed (v14 or higher).
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/) for package management.
- [PostgresSQL](https://www.postgresql.org/) installed and running.
- [Prisma CLI](https://www.prisma.io/docs/reference/tools-and-interfaces/prisma-cli) installed (`npm install -g prisma`).
- API Key from the external payment provider: KYl5kEN0Hl3sQKd4oIs7OfkB6qnN.

### Environment Configurations

Create a `.env` file in the project root and add the following environment variables:

```
DATABASE_URL=your_postgres_database_url
PAYMENT_PROVIDER_API_KEY=KYl5kEN0Hl3sQKd4oIs7OfkB6qnN
PAYMENT_PROVIDER_API_BASE_URL=https://xyz.com/v1
CALLBACK_URL=https://xyz.com/v1/payment/callback
SHARED_JWT_SECRET=mysecret-demo
```

Replace `your_postgres_database_url` with the actual URL of your PostgreSQL database.

## Getting Started

Follow these steps to set up and run the MOMO Payment Processor:

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/momo-payment-processor.git
   ```

2. Install dependencies:

   ```bash
   cd momo-payment-processor
   npm install
   ```

3. Set up your environment variables as described in the [Prerequisites](#prerequisites) section.

4. Run Prisma migrations to create the database schema:

   ```bash
   npx prisma migrate dev
   ```

5. Start the server:

   ```bash
   npm run start:dev
   ```

## Usage

To use the MOMO Payment Processor, follow these steps:

1. Make POST requests to save payments with the required details (amount, payment method, phone number, operator, and reference).
2. Clients can view their payment history by making relevant GET requests.
3. The processor will interact with the external payment provider to update the payment status.

## Contributing

We welcome contributions to improve the MOMO Payment Processor. If you'd like to contribute:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your changes to your fork.
5. Create a pull request to the main repository.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

This Markdown content represents what your README will look like when rendered properly in Markdown viewers or GitHub. You can copy and paste this into your project's README.md file.
