# zithon-chat

## ⚙️ Ideal Setup for Anonymous + Fast Messaging

## ✅ 1. Frontend (Vercel-Optimized)
1. Next.js (React + SSR/ISR support)

2. Tailwind CSS for fast styling

3. monero-javascript to manage wallet features directly in-browser

4. Use tweetnacl for client-side encryption (sign + encrypt messages)

5. Store public keys locally in browser or cache — no database

## ✅ 2. Server (for WebSocket & Wallet Relay)
You need a minimal backend off-Vercel (because Vercel doesn't support persistent WebSocket connections):

1. Use Node.js with Socket.IO for real-time messaging

2. Host it on Railway, Fly.io, Render, or even Cloudflare Workers with Durable Objects

3. Keep messages in RAM only or discard after delivery

Additional Security Measures:

1. Monero wallet-rpc integration (e.g., running wallet-rpc on a hidden VPS)

2. Rate-limiting or signature-based message verification

## ✅ Encryption Layer
1. tweetnacl or libsodium in both frontend and backend

2. Use public key encryption for E2EE (X25519 + Secretbox)

3. Optional: implement perfect forward secrecy by rotating session keys