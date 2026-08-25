# Acme Marketplace — Admin Dashboard

This repository contains the administrative control surface for the **Acme Marketplace**. It is a headless, React-based Single Page Application (SPA) built using the [Refine](https://refine.dev/) framework and [Material UI (MUI)](https://mui.com/).

The dashboard connects directly to the NestJS REST API, providing platform administrators with the tools necessary to manage the entire marketplace ecosystem — from dispute resolution to releasing Stripe seller payouts.

## Key Features

The admin dashboard empowers platform administrators to manage the multi-vendor marketplace at scale:

- **Order Oversight:** View complete order lifecycles, track shipping statuses, and monitor cross-vendor transactions.
- **Payout Approvals:** Manually review and release seller payouts via Stripe Connect to ensure a dispute window before funds are distributed.
- **Dispute Resolution:** Manage and resolve disputes between buyers and sellers, tracking evidence and enforcing outcomes.
- **Maker Verification:** Review incoming seller applications, verifying authenticity before granting them the verified artisan badge.
- **Platform Fee Configuration:** Dynamically configure platform commission rates and payment processing structures.
- **Support Ticket Management:** Handle incoming buyer and seller inquiries with a fully integrated ticketing interface.
- **Real-time Metrics:** Visualize key business metrics (GMV, active sellers, order volume) using `Recharts` and live data feeds.

## Tech Stack

- **Framework:** React 19, Vite
- **Architecture:** Refine (Headless CRUD Framework)
- **UI Library:** Material UI (MUI)
- **Data Fetching:** Axios, `@refinedev/simple-rest`
- **Routing:** React Router v7
- **Forms & Validation:** React Hook Form, Zod
- **Charts & Data Visualization:** Recharts
- **Real-time Sync:** Socket.IO Client

## Local Development

### Prerequisites
- Node.js (v20 or higher)
- A running instance of the Acme Marketplace Backend (NestJS)

### Setup

1. **Install dependencies:**
   ```bash
   npm install
   ```

2. **Configure Environment Variables:**
   Create a `.env` file in the root of the `admin-dashboard` directory (you can copy `.env.example`):
   ```env
   VITE_API_URL=http://localhost:8080
   VITE_MEDIA_URL=https://media.example.com/acme-marketplace-media
   VITE_APP_MAP_ID=your_map_id
   ```

3. **Start the development server:**
   ```bash
   npm run dev
   ```
   The dashboard will be available at `http://localhost:5173`.

## Build & Deployment

To build the application for production:
```bash
npm run build
```
This will generate optimized static assets in the `dist` directory, which are configured to be served directly from the NestJS backend's static directory in production, ensuring a unified deployment process.

---

> **Note:** This is a sanitized showcase version of a production project. All client-identifying details and secrets have been replaced with generic placeholders.
