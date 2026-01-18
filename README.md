# 🛡️ AstraGuard: Advanced Mission Control Dashboard

AstraGuard is a state-of-the-art, real-time satellite defense and monitoring system. Built for high-stakes aerospace operations, it provides deep situational awareness through immersive 3D visualizations, high-fidelity telemetry streaming, and AI-driven anomaly detection.

![Lighthouse Score](https://img.shields.io/badge/Lighthouse-95%2B-green.svg)
![Build Status](https://img.shields.io/badge/Build-Passing-brightgreen.svg)
![Tech Stack](https://img.shields.io/badge/Stack-Next.js%20|%20Three.js%20|%20FastAPI-blue.svg)

## 🏗️ System Architecture

AstraGuard is engineered as a distributed, high-performance system designed for sub-second latency and extreme reliability.

### 1. Immersive 3D Experience (Three.js/R3F)
- **Engine**: `@react-three/fiber` and `@react-three/drei` for GPU-accelerated rendering.
- **Scene Management**: A custom layer-based scene manager handling transitions from deep space (Galaxy) down to localized hardware (Monitor).
- **Asset Pipeline**: Optimized GLB loading with custom pre-compilation to prevent GPU stalls.
- **Shaders**: Custom GLSL implementation for planetary atmospheres, solar flares, and holographic HUD effects.

### 2. High-Frequency Telemetry (WebSocket)
- **Streaming**: Supports up to 5Hz real-time telemetry updates.
- **Resilience**: Automatic reconnection logic with exponential backoff and localized polling fallback.
- **State Buffer**: temporal state management for "Time Machine" replay capabilities.

### 3. AI-Driven Defense (Neural Core)
- **Anomaly Detection**: Real-time analysis of bus voltage, thermal fluctuations, and orbital drift.
- **Biometric Tracking**: High-contrast HUD alerts triggered by operator stress levels (simulated).
- **Prediction Engine**: Forecasts system failures before they occur via trend analysis.

## 🛠️ Tech Stack

- **Core**: Next.js 14+ (App Router), TypeScript.
- **Visuals**: Three.js, React Three Fiber, GSAP (Animations), Framer Motion.
- **Styling**: Tailwind CSS + Custom Vanilla CSS components.
- **Data**: Zustand (Global Store), React Context (Domain State).
- **Communication**: WebSockets (Real-time), REST (History & Metadata).

## 🚀 Deployment & Production

The application is optimized for **Vercel** with a specialized `vercel.json` configuration for environment-aware routing and static asset caching.

### Deploy to Vercel
1. Link your GitHub repo.
2. Ensure framework is set to **Next.js**.
3. Build Command: `npm run build`.

## 💻 Local Development

### 1. Installation
```bash
npm install
```

### 2. Run Locally
```bash
npm run mock    # Start the Mock WebSocket Backend (Port 8002)
npm run dev     # Start Next.js Development Server (Port 3000)
```

### 3. Verification
```bash
# Production Build Check
npm run build

# Type Safety Check
npx tsc --noEmit
```

## 🛰️ Module Overview

- **/components/experience**: Core 3D engine and scene assets.
- **/app/dashboard**: The Mission Control interface.
- **/app/hooks**: Domain-specific hooks for WebSockets, Debris tracking, and Space Weather.
- **/app/context**: Global application states (Navigation, Security, Dashboard).

---
**Authorized Personnel Only** • *AstraGuard Defense Systems v1.0*
