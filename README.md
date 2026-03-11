<!--
Park Capsule README — premium style
Tip: Works best with GitHub Dark Mode too.
-->

<div align="center">

<!-- Title -->
# 🚗🅿️ Park Capsule

 🌆 Smart Urban Parking — **Find • Book • Pay • Navigate**

**Park Capsule** is a full‑stack platform that helps drivers reserve nearby parking effortlessly and enables space owners to monetize unused parking spots.

<br/>

<!-- CTAs -->
<a href="https://park-capsule-new.vercel.app/"><b>🌐 Live Demo</b></a>
&nbsp;&nbsp;•&nbsp;&nbsp;
<a href="../../issues"><b>🐞 Report Bug</b></a>
&nbsp;&nbsp;•&nbsp;&nbsp;
<a href="../../issues"><b>✨ Request Feature</b></a>

<br/><br/>

<!-- Badges (clean & attractive) -->
<img alt="Next.js" src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white"/>
<img alt="React" src="https://img.shields.io/badge/React-0b1220?style=for-the-badge&logo=react&logoColor=61DAFB"/>
<img alt="Express" src="https://img.shields.io/badge/Express-111827?style=for-the-badge&logo=express&logoColor=white"/>
<img alt="Razorpay" src="https://img.shields.io/badge/Razorpay-0C2451?style=for-the-badge&logo=razorpay&logoColor=white"/>
<img alt="Google Maps" src="https://img.shields.io/badge/Google%20Maps-1a73e8?style=for-the-badge&logo=googlemaps&logoColor=white"/>
<img alt="Twilio" src="https://img.shields.io/badge/Twilio-F22F46?style=for-the-badge&logo=twilio&logoColor=white"/>

<br/><br/>

<!-- Aesthetic separator -->
<p>
  <i>Built for speed, simplicity, and smarter cities.</i>
</p>

</div>

## ✨ Why Park Capsule?

Parking in cities often means:
- ⏱️ wasting time searching
- ⛽ burning fuel unnecessarily
- 😤 dealing with uncertainty

**Park Capsule** solves this by connecting:
- 🚘 **Drivers** → discover & reserve spots quickly
- 🏡 **Owners** → list unused parking space and earn 💰

---

## 🚀 Features

🚗 Driver Experience
- 📍 Discover nearby parking slots
- 🅿️ Book a slot in seconds
- 💳 Smooth checkout with Razorpay
- 🧭 Get directions to the booked spot using Google Maps
- 📏 Auto-expand radius when slots are not available
- ⏳ Extend booking time with a simple flow

🏡 Owner Experience
- 💰 Monetize unused parking spaces
- 📅 Manage slot availability
- 📌 Handle bookings from users

---

## 🧠 How It Works

<details>
<summary><b>🔎 Expand to see the user journey</b></summary>

1) Discover 🔍
User searches parking near them (and can expand range when needed).

2) Reserve 🅿️
User selects a slot and confirms booking.

3) Pay 💳
Razorpay handles checkout securely.

4) Navigate 🧭
After payment, the app generates directions from the user’s location to the booked slot via Google Maps.

5) Extend ⏳
User can extend duration and complete remaining payment seamlessly.
</details>

---

## 🧰 Tech Stack

| Category | Tools |
|---|---|
| 🎨 Frontend | Next.js, React, Bootstrap / React-Bootstrap, Axios |
| 🛠️ Backend | Node.js, Express |
| 🗺️ Maps | Google Maps API (Maps + Directions) |
| 📌 Location | Geocoding API |
| 💳 Payments | Razorpay |
| 📲 Messaging | Twilio |


## 📁 Project Structure

> ✅ Frontend is present at: `park-capsule/`  
> 🛠️ Backend is described as: `backend/` (recommended).  
> If your backend is in another folder or repository, update the paths below.

```text
ParkCapsule-New/
├── README.md
├── park-capsule/                 # 🎨 Next.js Frontend
│   ├── components/
│   ├── context/
│   ├── pages/
│   ├── public/
│   ├── styles/
│   ├── next.config.js
│   ├── package.json
│   └── yarn.lock
└── backend/                      # 🛠️ Express Backend
    ├── package.json
    └── ...
```

---

## ⚙️ Getting Started

### ✅ Prerequisites
- 🟢 Node.js (recommended: 16+)
- 🧶 Yarn (frontend)
- 📦 npm (backend)

---

### 🔧 Setup & Run (Frontend)

```bash
git clone https://github.com/Vishnu2839/ParkCapsule-New.git
cd ParkCapsule-New/park-capsule

yarn install
yarn dev
```

✅ Frontend will run at:
- http://localhost:3000

---

### 🛠️ Setup & Run (Backend)

```bash
cd ../backend

npm install
npm run serve
```

✅ Backend typically runs at:
- http://localhost:5000

---

## 🔐 Environment Variables

### 🎨 Frontend: `park-capsule/.env.local`
```bash
NEXT_PUBLIC_API_BASE_URL=http://localhost:5000
NEXT_PUBLIC_GOOGLE_MAPS_API_KEY=your_google_maps_key
NEXT_PUBLIC_RAZORPAY_KEY_ID=your_razorpay_key_id
```

### 🛠️ Backend: `backend/.env`
```bash
PORT=5000

RAZORPAY_KEY_ID=your_razorpay_key_id
RAZORPAY_KEY_SECRET=your_razorpay_key_secret

TWILIO_ACCOUNT_SID=your_twilio_sid
TWILIO_AUTH_TOKEN=your_twilio_auth_token
TWILIO_PHONE_NUMBER=your_twilio_phone_number

GEOCODE_API_KEY=your_geocode_api_key
GOOGLE_MAPS_API_KEY=your_google_maps_key
```

> 🔒 **Security Tip:** Keep all secrets server-side. Never expose Razorpay secret keys or Twilio tokens in frontend variables.

---

## 🗺️ Google Maps API

Google Maps powers:
- 🗺️ map display for slots
- 🧭 route/directions from user → booked slot

✅ Common APIs to enable in Google Cloud:
- Maps JavaScript API
- Directions API
- Geocoding API
- Places API (optional)

---

## 💳 Payments (Razorpay)

- 💳 Frontend triggers Razorpay checkout
- ✅ Backend should verify payment & confirm booking
- 🅿️ Booking is finalized after successful payment verification

---

## 📲 Notifications (Twilio)

Twilio can be used for:
- 🔐 OTP verification
- 📩 booking confirmation messages
- ⏰ reminders / alerts

---

## 🛣️ Roadmap

- ⭐ Slot ratings & feedback
- 🚘 Vehicle rental option
- 📅 Advanced booking system


## 🤝 Contributing

Contributions are welcome! 🙌  
1. Fork the repo 🍴  
2. Create a branch: `git checkout -b feature/my-feature` 🌿  
3. Commit: `git commit -m "feat: add my feature"` ✅  
4. Push: `git push origin feature/my-feature` 🚀  
5. Open a PR 🔥

---

<div align="center">

### Made with ❤️ for smarter parking and smarter cities 🌆🅿️✨

</div>
