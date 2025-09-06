# TokenTracker Demo App with Civic Auth Integration

This project, **TokenTracker**, integrates Civic Auth as the single sign-on (SSO) provider to enable secure and seamless user authentication for a token tracking application.

## Project Description

MyTokenTracker uses uHTTP, powered by the HOPR protocol, to fetch and display the address’s mainnet balances on the screen. This happens without leaking any metadata, thanks to HOPR’s privacy layer (https://hoprnet.org)

## Features
- **Civic Auth Integration**: Implemented as the sole SSO provider for user authentication, ensuring a frictionless sign-in process.
- **Civic Embedded ETH Wallet**: Used to encrypt and decrypt securly the ETH Address of the SSO account owner
- **Token Data Endpoint**: Access token information via the `/logo/{TOKEN_ETHEREUM_ADDRESS}` endpoint.
- **Websocket Logs**: Real-time client logs available through the `/client_logs/websocket` endpoint.
- **Token List**: Sourced from `server/tokens.json` for reliable token data.
- **Public Demo**: Hosted on Vercel at [https://mytokentracker-xyz-civic.vercel.app/](https://mytokentracker-xyz-civic.vercel.app/).

## Civic Integration:
 - [Addtion of the Civic NPM package]()
 - [Integration of the Civic Embedded wallet using Viem]()
 - [Code that uses the Civic Embedded wallet for encrpting and decrypting private data](Integration of the Civic Embedded wallet using Viem)
 - [Civic Connect widget styles]()

## How to Run Locally
### Backend
1. Install dependencies:
   ```bash
   yarn
   ```
2. Start the backend:
   ```bash
   yarn start:be
   ```
   or use `wrangler dev` for development.

### Frontend
1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```
2. Install dependencies:
   ```bash
   yarn
   ```
3. Start the frontend:
   ```bash
   yarn start:fe
   ```

### Frontend Environment Variables
Create a `.env` file in the `frontend` directory with the following:
```plaintext
VITE_BACKEND_URL=backend.mytokentracker.xyz  //'127.0.0.1:8787' if local server is used
VITE_uHTTP_DP_ENDPOINT= //leave empty to use default
VITE_uHTTP_TOKEN=
VITE_uHTTP_FORCE_ZERO_HOP=true
VITE_CIVIC_CLIENT_ID=
VITE_JSONBIN_API_KEY=
```

## Contributors
- Michal Jadach (michal.jadach@hoprnet.org)
- Andrius Stepaitis (andrius@hoprnet.org)

## YouTube Demo Video
A demo video showcasing the integration of Civic Auth and the user experience of TokenTracker is available here: [YOUTUBE_LINK]

## Live Demo
The application is deployed and publicly accessible at:  
[https://mytokentracker-xyz-civic.vercel.app/](https://mytokentracker-xyz-civic.vercel.app/)

