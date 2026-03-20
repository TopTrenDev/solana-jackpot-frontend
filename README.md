# Solana Jackpot Frontend (Tower)

Next.js (Pages Router) frontend for the Tower Jackpot game. The UI connects to the backend over WebSockets and builds Anchor transactions to interact with on-chain programs via the user wallet.

## Tech Stack

- Next.js + React + TypeScript
- Tailwind CSS + Sass
- Solana Wallet Adapter (`@solana/wallet-adapter-*`)
- Anchor (`@project-serum/anchor`)
- `socket.io-client`, `axios`, `@tanstack/react-query`

## Prerequisites

- Node.js 20+

## Setup

Install dependencies:

```bash
npm install
```

## Development

```bash
npm run dev
```

## Lint

```bash
npm run lint
```

## Production Build

```bash
npm run build
```

Start the production server:

```bash
npm run start
```

> Note: `npm run start` uses the port defined in `package.json` (`next start -p 4578`).

## Configuration

Update runtime endpoints and RPC in `src/config.tsx`:

- API base URLs (e.g. `API_URL`, `GRAVE_API_URL`, `INFINITE_API_URL`)
- Socket URLs (e.g. `SOCKET_URL`, `GRAVE_SOCKET_URL`, `INFINITE_SOCKET_URL`)
- RPC endpoint (`RPC_URL`)

Wallet/network selection is configured in `src/components/wallet/Wallet.tsx` (currently `WalletAdapterNetwork.Mainnet`).

## Troubleshooting

- Wallet does not connect: verify your wallet extension injects `window.solana` and that it supports transaction signing.
- No real-time updates: verify the socket URLs in `src/config.tsx` and confirm the backend emits the expected socket events.

## Contact

If you need help:

[![Telegram](https://img.shields.io/badge/Telegram-@toptrendev_66-2CA5E0?style=for-the-badge&logo=telegram)](https://t.me/TopTrenDev_66)
[![Twitter](https://img.shields.io/badge/Twitter-@toptrendev-1DA1F2?style=for-the-badge&logo=x)](https://x.com/intent/follow?screen_name=toptrendev)
