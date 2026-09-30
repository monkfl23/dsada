# Lobex Service

Minimal production-oriented SMM panel starter.

## Run

Ubuntu/Debian:

```bash
sudo apt update
sudo apt install -y nodejs npm
npm install
cp .env.example .env
# change SESSION_SECRET in .env
npm start
```

The app listens on **port 3400**.

Open:
`http://SERVER_IP:3400`

Admin:
- Username: `Lobex`
- Password: `Lopix_MDN12314(67657692`

Admin API endpoints are ready for provider/category/service management. Provider API keys are server-side only.

## Cloudflare Tunnel

Point the tunnel ingress to:

`http://127.0.0.1:3400`

Do not expose the provider API keys to the frontend.

## Important

The SMM adapter expects a common `action/key` form and supports:
- `balance`
- `services` (endpoint available for extension)
- `add`
- `status`

Provider-specific differences may require an adapter adjustment. Test against your actual provider before accepting real customer orders.
