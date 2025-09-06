# tokentracker-demo-app extended with Civic Auth a seamless user management 

## Made during and for ETHWarsaw 2025 hackathon

Logo Endpoint: `/logo/{TOKEN_ETHEREUM_ADDRESS}`

Websocket Logs Endpoint: `/client_logs/websocket`

Token list is taken from `server/tokens.json`

## Run locally

Backend:


```bash
yarn
wrangler dev
```

or if dependencies are installed:

```bash
yarn start:be
```

Frontend:

```bash
cd frontend
yarn
yarn dev
```

or if dependencies are installed:

```bash
yarn start:fe
```

## Front-end .env:

```
VITE_BACKEND_URL=backend.mytokentracker.xyz  //'127.0.0.1:8787' if local server is used
VITE_uHTTP_DP_ENDPOINT= //leave empty to use default
VITE_uHTTP_TOKEN=
VITE_uHTTP_FORCE_ZERO_HOP=true
VITE_CIVIC_CLIENT_ID=
VITE_JSONBIN_API_KEY=

```