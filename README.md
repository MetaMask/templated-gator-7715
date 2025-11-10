# NextJS Advanced Permissions Starter

This is a NextJS Advanced Permissions (ERC-7715) starter created with [@metamask/create-gator-app](https://www.npmjs.com/package/@metamask/create-gator-app).

This template is meant to help you bootstrap your own projects with [Metamask Smart Accounts Kit](https://docs.metamask.io/smart-accounts-kit/). It helps you build smart accounts with account abstraction, and powerful delegation features.

Learn more about [Metamask Smart Accounts Kit](https://docs.metamask.io/smart-accounts-kit/).

## Prerequisites

1. **Pimlico API Key**: In this template, we use Pimlico's Bundler and Paymaster services to submit user operations and sponsor transactions, respectively. You can retrieve the required API key from [Pimlico's Dashboard](https://dashboard.pimlico.io/apikeys).

2. **RPC URL** In this template, you’ll need an RPC URL for the Sepolia chain. You can use any preferred RPC provider or a public RPC. However, we recommend using a paid RPC to ensure better reliability and avoid potential rate-limiting issues.

## Project Structure

```bash
erc7715-starter/
├── public/ # Static assets
├── src/
│ ├── app/ # App router pages
│ ├── components/ # UI Components
│ │ ├── CreateSessionAccount.tsx # Component for creating a session account
│ │ ├── GrantPermissionsButton.tsx # Component for granting permissions
│ │ ├── Hero.tsx # Hero section component
│ │ ├── InstallFlask.tsx # Component for installing MetaMask Flask
│ │ ├── Loader.tsx # Loading indicator component
│ │ ├── PermissionInfo.tsx # Component for displaying permission information
│ │ ├── RedeemPermissionButton.tsx # Component for redeeming permissions
│ │ ├── Steps.tsx # Step-by-step guide component
│ │ └── WalletInfoContainer.tsx # Component for displaying wallet information
│ ├── providers/ # React Context Providers
│ │ ├── PermissionProvider.tsx # Provider for permission state
│ │ └── SessionAccountProvider.tsx # Provider for session account state
│ ├── services/ # Service layer for API interactions
│ └── config.ts # Configuration settings
├── .env # Environment variables
├── .gitignore # Git ignore rules
├── next.config.ts # Next.js configuration
├── postcss.config.mjs # PostCSS configuration
├── tailwind.config.ts # Tailwind CSS configuration
└── tsconfig.json # TypeScript configuration
```

## Setup Environment Variables

Update the following environment variables in the `.env` file located in your project's root directory.

```
NEXT_PUBLIC_PIMLICO_API_KEY =
```

## Getting Started

First, start the development server

```bash
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Application Flow

This template demonstrates a complete MetaMask Advanced Permissions (ERC-7715) flow:

1. **Create Session Account**: Users can create a session account that will be used to redeem permissions.
2. **Grant Permissions**: Users can grant Advanced Permissions to the session account.
3. **Redeem Permissions**: The session account can use the granted permissions to perform actions on behalf of the MetaMask user.

## Learn More

To learn more about Smart Accounts Kit, take a look at the following resources:

- [Advanced Permissions (ERC-7715) guide](https://docs.metamask.io/smart-accounts-kit/guides/advanced-permissions/execute-on-metamask-users-behalf/) - Learn how to use MetaMask Adanved Permissions.
- [Smart Accounts Kit Documentation](https://docs.metamask.io/smart-accounts-kit/) - Learn more about Smart Accounts Kit features and API.
