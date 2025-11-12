Perfect — the visual references you’ve uploaded clearly show the **Liquid Glass UI aesthetic** you want: transparent floating cards, soft frosted blur, no solid background, and colorful, high-contrast text with a 3D “pop-out” glow effect.

Below is the **fully rewritten master prompt** for **Cursor IDE** to build your **COCCE Super App** using **React Native + Capacitor** with this **Liquid Glass UI design**.

---

## 💎 COCCE Super App — React Native + Capacitor Hybrid with Liquid Glass UI (Final Build Prompt)

**Goal:**
Build a **hybrid mobile super app** called **COCCE Super App**, using **React Native + Capacitor** (Android & iOS) with **TypeScript**, **Supabase**, and **Bunny.net**.
The entire interface must follow a **Liquid Glass Design Language** — blurred, transparent, layered glass cards and buttons that appear to *float above the background*, with **no solid backgrounds** and **colorful, luminous fonts/icons** for readability and depth.

---

### 🧰 Core Architecture

| Layer            | Technology                                        |
| ---------------- | ------------------------------------------------- |
| Framework        | React Native (latest stable)                      |
| Native Runtime   | Capacitor (Android + iOS)                         |
| Language         | TypeScript                                        |
| Backend          | Supabase (Auth, Database, Realtime, Functions)    |
| Storage          | Bunny.net (images, audio, documents)              |
| Video Streaming  | Bunny.net Stream (videos for feed, shop, stories) |
| Payments         | Google Play Billing / App Store In-App Purchases  |
| Design           | Liquid Glass UI + Colorful Typography             |
| State Management | Zustand / Redux Toolkit                           |
| Styling          | NativeWind (Tailwind CSS)                         |
| Navigation       | React Navigation (Bottom Tabs)                    |

---

### ✨ Liquid Glass UI Guidelines

* **No solid backgrounds:** use `rgba(255,255,255,0.05)` to `rgba(255,255,255,0.15)` with heavy blur (`backdrop-filter: blur(20-30px)` or `blur-md`/`blur-xl` in Tailwind).
* **Cards and buttons**: rounded (2xl or 3xl), layered shadows, glowing borders, and elevation to appear *floating*.
* **Fonts:** bright, colorful gradients (teal, magenta, cyan, lime, orange) for contrast.
* **Icons:** luminous with subtle neon outline.
* **Focus on depth:** use multiple transparency layers and shadows for realism.
* **Reference Images:**

  * `/mnt/data/iphone17-liquid-glass.jpg`
  * `/mnt/data/still-ac51633ed21b661e746652dacce1a70a.jpg`

---

### 🧭 Navigation Structure (Bottom Tabs)

1. **Feed** — TikTok-like vertical video feed (autoplay, native player)
2. **Shop** — Social commerce marketplace with product videos
3. **Upload** — Capture or upload new videos (native camera & mic)
4. **Wallet** — COCCE COIN payments, charts, and QR codes
5. **Profile** — User profile, campaigns, and VIP status

---

### 🔐 Onboarding & Authentication

* Full-screen **liquid glass form** with smooth native transitions
* Fields: full name, username, country, city, birthdate, gender, phone, email, profile photo
* Supabase Auth (email/password + phone OTP)
* Profile images stored in Bunny.net → `profiles/`
* Blur background with layered colorful typography for title and buttons

---

### 🎥 Feed Page

* Vertical **autoplay feed** powered by Bunny.net Stream (native player)
* Transparent top search bar
* Floating buttons for:

  * Messages (chat, stories)
  * Legends (trending shops, products, videos)
  * Comments (text, voice, image, video replies)
* Likes and Loves tracked in Supabase
* Comments stored in Bunny.net → `comments/`

---

### 🛍️ Shop Page

* Autoplaying **product videos** from Bunny.net Stream
* **Floating Action Buttons (FABs)** with liquid glass style:

  * Right: WhatsApp, Call, Text, Order, Comment, Add to Cart
  * Left: Manage Shops, Add Shop/Product, View Cart, Buy via USSD
* **Shop Creation Form:** logo, name, description, contact, location, payment numbers
* **Product Creation Form:** shop selection, name, price, description, video, tags
* **Campaigns (visibility engine):**

  * Promote Feed Videos, Product Videos, or Shops
  * Duration: 3, 7, or 14 days
  * Region or global targeting
  * Paid with COCCE COIN

**Bunny.net Folders:**

```
shop-logos/
products/
videos/
thumbnails/
```

---

### 📤 Upload Page

* Record or upload video using **Capacitor Camera + Microphone**
* Fields: title, description, hashtags, location, visibility, collaborators
* Upload videos → Bunny.net Stream (`videos/`)
* Store thumbnail → `thumbnails/`
* Notify collaborators via Supabase Realtime

---

### 💬 Messages & Stories

#### Messages

* Real-time chat via Supabase Realtime
* Support text, image, audio, video, and docs
* All media stored in Bunny.net → `messages/`

#### Stories

* Image and video stories stored in Bunny.net → `stories/`
* Auto-deletes after 24 hours via Supabase scheduled function

---

### 💰 Wallet Page (COCCE COIN)

* Display COCCE COIN balance
* Buy coins via **Google Play Billing** or **App Store IAP**
* 1 COCCE COIN = 1 TZS
* Show spending charts and analytics
* Send coins to others via QR scan or username
* Static QR codes stored in Bunny.net → `qr-codes/`

---

### 👤 Profile Page

* Floating **squircle profile photo** with blurred glass background
* Buttons: Manage Profile, Shops, Campaigns, VIP Badge
* **VIP Badge:** 10,000 COCCE COINS for 60 days

  * Adds golden shield & weekly feed/video visibility boost
* Manage uploaded videos, products, and shops
* Settings: edit profile, logout

---

### 📊 Campaign System (Visibility Engine)

* Campaign Types:

  * Feed Video Promotion
  * Product Video Boost
  * Shop Visibility Boost
* Cost: 1 COCCE COIN = 1 View
* Duration: 3, 7, or 14 days
* Targeting: region, Tanzania, East Africa, or global
* Realtime tracking in Supabase (coins, views, duration, engagement)

---

### 🧱 Backend Integration

**Supabase**

* Auth (email/password or OTP)
* Database: profiles, shops, products, campaigns, messages, wallet, analytics
* Realtime: chat, notifications, and analytics
* Functions:

  * Story auto-deletion (24h)
  * Campaign tracking and coin deduction

**Bunny.net**

* Storage (images, audio, docs)
* Stream (videos)
* CDN for fast delivery
* Secure token-based URLs

**Folder Structure:**

```
comments/
messages/
products/
profiles/
qr-codes/
shop-logos/
stories/
thumbnails/
videos/
```

---

### ⚡ Capacitor Plugins

```bash
npm install @capacitor/core @capacitor/cli
npm install @capacitor/camera @capacitor/media @capacitor/filesystem
npm install @capacitor/haptics @capacitor/device @capacitor/app
npm install capacitor-google-payments capacitor-ios-payments
npx cap add android
npx cap add ios
```

**capacitor.config.ts**

```ts
import { CapacitorConfig } from '@capacitor/cli';

const config: CapacitorConfig = {
  appId: 'com.cocce.superapp',
  appName: 'COCCE Super App',
  webDir: 'dist',
  bundledWebRuntime: false,
  plugins: {
    Camera: { saveToGallery: true },
    Media: { allowEditing: true },
  },
};

export default config;
```

---

### 🧠 Development Stack Summary

| Feature   | Stack                                |
| --------- | ------------------------------------ |
| UI        | React Native + NativeWind (Tailwind) |
| Backend   | Supabase                             |
| Storage   | Bunny.net                            |
| Streaming | Bunny.net Stream                     |
| Payments  | Play Billing + iOS IAP               |
| Auth      | Supabase Auth (Email + OTP)          |
| Design    | Liquid Glass UI                      |
| State     | Zustand / Redux Toolkit              |

---

### 🧬 Deliverable

A futuristic **React Native + Capacitor hybrid app** for Android & iOS featuring:

* Liquid Glass UI (transparent, floating, colorful)
* COCCE COIN payment economy
* Supabase + Bunny.net backend
* Native player, camera, and mic integration
* 24-hour stories, realtime messaging
* Campaign-driven visibility system

read these to get better understanding
@https://developer.android.com/      @https://archive.reactnative.dev/docs/next/getting-started    @https://docs.bunny.net/ @https://supabase.com/docs 
