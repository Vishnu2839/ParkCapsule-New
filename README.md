<div align="center">

# Park Capsule

A modern urban parking platform to **find, book, and pay for parking** — and to help **space owners monetize unused parking spots**.

[Live Demo](https://park-capsule-new.vercel.app/) · [Issues](../../issues)

</div>

## About

**Park Capsule** is built to reduce the friction of urban parking by connecting:

- **Drivers** who need to quickly find and book nearby parking
- **Space owners** who want to list unused space and earn from it

It provides a smooth experience from discovery → booking → payment → navigation.

---

## Features

- Book parking slots near your location with hassle-free payments
- List your unused space as a parking spot and earn money
- Auto-increase search radius when nearby slots are unavailable
- Get directions to the booked slot after payment
- Extend booking time and complete payment in just a few clicks

---

## Tech Stack

**Frontend**
- Next.js
- React
- Bootstrap / React-Bootstrap
- Axios

**Backend**
- Express (Node.js)

**Integrations**
- Razorpay (Payments)
- Google Maps API (Maps + Directions / location flow)
- Geocoding API
- Twilio (Notifications)

---

## Architecture (High Level)

- **Frontend (Next.js)** handles UI, booking flow, and map rendering.
- **Backend (Express)** provides APIs for parking slot management, bookings, payments, and integrations.
- **Google Maps API** powers map display and directions to the booked slot.
- **Razorpay** processes payments and confirms booking.
- **Twilio** can be used for OTP/alerts/notifications (based on your setup).

---

## Project Structure

> Your repo currently contains the frontend inside `park-capsule/`.  
> This README describes the **full project** (frontend + backend).  
> If your backend exists in a different folder/repo, place it under `backend/` (recommended) or update paths accordingly.

```text
ParkCapsule-New/
├── README.md
├── park-capsule/                 # Frontend (Next.js)
│   ├── components/
│   ├── context/
│   ├── pages/
│   ├── public/
│   ├── styles/
│   ├── next.config.js
│   ├── package.json
│   └── yarn.lock
└── backend/                      # Backend (Express)  <-- add/ensure this exists
    ├── package.json
    ├── src/
    └── ...
```

---

## Getting Started (Run Locally)

### Prerequisites
- Node.js (recommended: 16+)
- Yarn (for frontend)
- npm / yarn (for backend)

---

## Frontend Setup

```bash
git clone https://github.com/Vishnu2839/ParkCapsule-New.git
cd ParkCapsule-New/park-capsule

yarn install
yarn dev
```

Frontend runs at:
- http://localhost:3000

---

## Backend Setup

> If your backend folder name is different, replace `backend` below.

```bash
cd ParkCapsule-New/backend

npm install
npm run serve
```

Backend typically runs at something like:
- http://localhost:5000 (example)

---

## Environment Variables

Create environment files for both apps.

### Frontend (`park-capsule/.env.local`)
```bash
# Backend API
NEXT_PUBLIC_API_BASE_URL=http://localhost:5000

# Google Maps API Key (client-side)
NEXT_PUBLIC_GOOGLE_MAPS_API_KEY=your_google_maps_key

# Razorpay public key (client-side)
NEXT_PUBLIC_RAZORPAY_KEY_ID=your_razorpay_key_id
```

### Backend (`backend/.env`)
```bash
# Server
PORT=5000

# Razorpay (server-side secrets)
RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret

# Twilio (optional)
TWILIO_ACCOUNT_SID=your_twilio_sid
TWILIO_AUTH_TOKEN=your_twilio_token
TWILIO_PHONE_NUMBER=your_twilio_number

# Google / Geocoding (if called from backend)
GOOGLE_MAPS_API_KEY=your_google_maps_key
GEOCODE_API_KEY=your_geocode_key
```

> Keep secrets in backend `.env` only. Never expose secret keys in the frontend.

---

## Google Maps API

This project uses **Google Maps API** to:
- Show maps for slot location
- Provide directions to the booked slot
- Support location-based discovery (and optionally geocoding)

You typically need to enable in Google Cloud:
- Maps JavaScript API
- Places API (optional, if used)
- Directions API (if used)
- Geocoding API (if used)

---

## Payments

Payments are handled via **Razorpay**:
- Frontend collects payment with Razorpay checkout
- Backend validates and confirms payment (recommended approach)
- Booking is finalized after successful payment confirmation

---
