# TokenTracker Demo App with Civic Auth Integration

This project, **TokenTracker**, integrates Civic Auth as the single sign-on (SSO) provider to enable secure and seamless user authentication for a token tracking application.

## Project Description

MyTokenTracker lets users track Ethereum EOA wallet assets privately by not leaking metadata and without accessing blockchain data directly.

## Features
- **Civic Auth Integration**: Implemented as the sole SSO provider for user authentication, ensuring a frictionless sign-in process.
- **Token Data Endpoint**: Access token information via the `/logo/{TOKEN_ETHEREUM_ADDRESS}` endpoint.
- **Websocket Logs**: Real-time client logs available through the `/client_logs/websocket` endpoint.
- **Token List**: Sourced from `server/tokens.json` for reliable token data.
- **Public Demo**: Hosted on Vercel at [https://mytokentracker-xyz-civic.vercel.app/](https://mytokentracker-xyz-civic.vercel.app/).

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
REACT_APP_BACKEND_URL=tokentracker.hoprnet.workers.dev  # Use '127.0.0.1:8787' for local server
REACT_APP_uHTTP_DP_ENDPOINT=  # Leave empty to use default
REACT_APP_uHTTP_TOKEN=
REACT_APP_uHTTP_FORCE_ZERO_HOP=true
```

## Contributors
- Michal Jadach (michal.jadach@hoprnet.org)
- Andrius Stepaitis (andrius@hoprnet.org)

## YouTube Demo Video
A demo video showcasing the integration of Civic Auth and the user experience of TokenTracker is available here: [YOUTUBE_LINK]

## Live Demo
The application is deployed and publicly accessible at:  
[https://mytokentracker-xyz-civic.vercel.app/](https://mytokentracker-xyz-civic.vercel.app/)
