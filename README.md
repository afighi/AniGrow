<div align="center">

#  AniGrow Mobile

### **AI-Powered Poultry and Livestock Farming Guide with Data Analytics**

[![React Native](https://img.shields.io/badge/React%20Native-0.81.5-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://reactnative.dev/)
[![Expo](https://img.shields.io/badge/Expo%20SDK-54-000020?style=for-the-badge&logo=expo&logoColor=white)](https://expo.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.9-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Supabase](https://img.shields.io/badge/Supabase-Backend%20%26%20DB-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)](https://supabase.com/)
[![TailwindCSS](https://img.shields.io/badge/NativeWind-Tailwind%20v3-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://nativewind.dev/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge)](LICENSE)

<br/>

**AniGrow** is an end-to-end mobile agricultural technology platform tailored for modern farmers and livestock managers. Built with **React Native**, **Expo**, and **Supabase**, it unifies automated livestock growth tracking, IoT smart-scale data synchronization, AI-powered health recommendations, and real-time herd analytics into a fluid, user-friendly mobile experience.

</div>

---

## 🌟 Key Highlights & Features

### ⚖️ Real-Time Smart Weighing & IoT Integration
- **Direct Weight Ingestion:** Seamless integration with digital scales and feeder sensors to capture animal weigh-ins instantly.
- **Simulation & Calibration Mode:** Built-in weighing simulator and threshold calibrator for field testing and remote debugging.
- **Growth Standards Comparison:** Automatically compares live weights against industry standard growth trajectories (Swine, Broilers, Layers) to highlight outliers.

### 🤖 AniBot — Multimodal AI Farming Assistant
- **Voice, Text & Image Diagnosis:** Powered by Gemini AI, AniBot analyzes user questions, voice prompts, and livestock photos (e.g. skin abnormalities, posture, eye conditions).
- **Proactive Health Insights:** Delivers feed conversion ratio (FCR) optimizations, vaccination schedule alerts, and symptom assessment suggestions.

### 📊 Livestock Management & Growth Analytics
- **Individual & Batch Tagging:** Detailed profiles for livestock including Ear Tag IDs, breed, birth date, batch, health records, and current pen.
- **Growth Curve Visualizations:** Interactive chart kits tracking historical weight gain against target growth velocity.
- **Feed & Supply Consumption Tracking:** Log daily rations, monitor inventory depletion, and calculate feed efficiency across distinct life stages.

### 🏥 Herd Health & Medical Logs
- **Vaccination Schedules & Alerts:** Automated reminders for routine immunizations and biosecurity protocols.
- **Illness & Quarantine Tracking:** Instant isolation flagging, medication administration history, and recovery checkpoints.

### ☁️ Cloud Synced & Offline Tolerant
- **Supabase PostgreSQL & Realtime:** Instant multi-device sync, row-level security (RLS), and secure authentication.
- **Resilient Local Caching:** AsyncStorage caching ensures essential herd data remains accessible even in low-connectivity rural farm environments.

---

## 🛠️ Architecture & Tech Stack

| Layer | Technologies |
| :--- | :--- |
| **Mobile Core** | [React Native 0.81](https://reactnative.dev/), [Expo SDK 54](https://expo.dev/) |
| **Navigation & Routing** | [Expo Router v6](https://docs.expo.dev/router/introduction/) (Typed file-based routing) |
| **Language** | [TypeScript](https://www.typescriptlang.org/) (Strict typing & safety) |
| **Styling & Design System** | [NativeWind v4](https://www.nativewind.dev/) + [Tailwind CSS](https://tailwindcss.com/), [React Native Paper](https://callstack.github.io/react-native-paper/) |
| **Icons & Media** | [Phosphor Icons](https://phosphoricons.com/), `@expo/vector-icons`, `react-native-svg` |
| **Animations & Interactions** | [React Native Reanimated v4](https://docs.swmansion.com/react-native-reanimated/), Gesture Handler |
| **Backend & Database** | [Supabase](https://supabase.com/) (PostgreSQL, Row Level Security, Realtime, Storage) |
| **AI Integration** | Google Gemini Generative AI (Vision, Voice & Text Analysis) |
| **Device Hardware APIs** | `expo-camera`, `expo-image-picker`, `expo-av`, `expo-notifications`, `expo-haptics`, `expo-print` |
| **Build & Release** | Expo Application Services (EAS Build) |

---

## 📂 Project Structure

```bash
Ani-grow-v2/
├── app/                      # Expo Router navigation hierarchy
│   ├── (ai)/                 # AniBot AI assistant screens & voice/image chat
│   ├── (analytics)/          # Herd growth metrics, charts, & performance reports
│   ├── (animals)/            # Livestock management, registration, & profiles
│   ├── (auth)/               # Login, registration, & account verification
│   ├── (dashboard)/          # Primary farm overview & activity feeds
│   ├── (devices)/            # IoT smart scales, feeders, & connection management
│   ├── (guide)/              # Best practices & breed standards knowledge base
│   ├── (health)/             # Medical logs, quarantine, & treatment tracking
│   ├── (weighing)/           # Live weighing sessions & recording workflows
│   ├── _layout.tsx           # Global root layout, providers, & navigation stack
│   └── index.tsx             # Entry routing logic
├── src/
│   ├── components/           # Reusable UI component library (cards, inputs, modals)
│   ├── constants/            # Breed standards, feeding tables, theme tokens
│   ├── context/              # Global React contexts (Auth, Farm, Devices)
│   ├── hooks/                # Custom hooks for Supabase realtime & device sensors
│   ├── lib/                  # Client configs (Supabase client, Gemini API, helpers)
│   ├── styles/               # Theme definitions & global style constants
│   └── types/                # Domain models, database types, & navigation routes
├── assets/                   # App icons, splash screens, & branding assets
├── app.json                  # Expo project manifest & native permissions configuration
├── eas.json                  # EAS Build & deployment pipelines
└── tailwind.config.js        # Tailwind CSS & theme tokens configuration
```

---

## 🚀 Getting Started

Follow these steps to set up the project locally for development:

### 1. Prerequisites
- **Node.js**: `v18.x` or higher
- **Package Manager**: `npm`, `yarn`, or `pnpm`
- **Expo Go** app on your physical mobile device (iOS/Android), or an iOS Simulator / Android Emulator

### 2. Clone the Repository
```bash
git clone https://github.com/afighi/AniGrow.git
cd AniGrow
```

### 3. Install Dependencies
```bash
npm install
```

### 4. Configure Environment Variables
Create a `.env` file in the root directory (based on `.env.example`):
```bash
cp .env.example .env
```
Fill in your Supabase and Gemini credentials:
```env
EXPO_PUBLIC_SUPABASE_URL=your_supabase_project_url
EXPO_PUBLIC_SUPABASE_ANON_KEY=your_supabase_anon_key
EXPO_PUBLIC_GEMINI_API_KEY=your_gemini_api_key
```

### 5. Run the Application
Start the Expo development server:
```bash
npm start
# or
npx expo start -c
```
- Scan the QR code using the **Expo Go** app on iOS/Android.
- Press `a` to launch in Android Emulator.
- Press `i` to launch in iOS Simulator.
- Press `w` to open in Web view.

---

## 🧪 Available Scripts

| Command | Purpose |
| :--- | :--- |
| `npm start` | Launches the Expo development server |
| `npm run android` | Builds and runs on a connected Android device/emulator |
| `npm run ios` | Builds and runs on an iOS simulator |
| `npm run web` | Runs the web-compiled preview |
| `npm run lint` | Runs ESLint checks across the codebase |

---

## 👤 Author

**Ahiah R.D.G. (afighi)**
- **GitHub:** [@afighi](https://github.com/afighi)
- **Portfolio:** [Fullstack Developer Portfolio](https://github.com/afighi)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE) — see the LICENSE file for details.
