# Oorva / Re:Root – Civic EcoCommerce & Smart Cleanup

Oorva/Re:Root powers NGO-led cleanups, community gardening, and farm-help missions, and connects those actions to a sustainable marketplace. Volunteers log geo-tagged missions with before/after verification; NGOs manage events and export sponsor-ready impact reports; sponsors fund missions with transparent proof; eco-sellers and nurseries accept volunteer vouchers.

## Apps
- `apps/web` – Next.js site + partner consoles (NGO, Seller, CSR, Admin)
- `apps/mobile` – React Native/Expo volunteer app

## Services
- `services/api-gateway` – Public API / BFF
- `services/mission-service` – Missions, verification, points/wallet
- `services/marketplace-service` – Catalog, orders, vouchers, payouts
- `services/csr-service` – Sponsors, invoices, reports
- `services/ml-service` – Waste severity (CNN), geo-hotspots (DBSCAN/OPTICS)

## Shared Packages
- `packages/ui`, `packages/utils`, `packages/config`, `packages/types`

## Infra
- Firebase Auth & Storage, Firestore or Postgres (via Prisma), Razorpay/Stripe

## Quick Start
```bash
# install toolchain
corepack enable || npm i -g pnpm
pnpm install

# envs
cp .env.example .env

# dev (in parallel)
pnpm -w dev
