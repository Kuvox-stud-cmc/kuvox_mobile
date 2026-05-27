# kuvox-mobile

The mobile client of **Kuvox** — a graph-augmented retrieval system for intelligent
video editing. This is a React Native application built with Expo that provides a
mobile-optimized interface for video browsing, project management, and
conversational editing commands. It communicates with the ASP.NET business backend
via REST and WebSocket.

## Tech stack

- **React Native** via **Expo** (managed workflow)
- **Expo Router** (file-based routing)
- **TypeScript** (strict mode)
- **Expo AV** for media playback

## Prerequisites

- Node.js **20+** (LTS recommended)
- npm (ships with Node)
- Expo CLI (`npx expo`)
- For device testing: Expo Go app on iOS/Android, or a development build

## Getting started

```bash
# Install dependencies
npm install

# Start the Expo dev server
npx expo start
```

From the dev server output you can open the app in:

- A [development build](https://docs.expo.dev/develop/development-builds/introduction/)
- An [Android emulator](https://docs.expo.dev/workflow/android-studio-emulator/)
- An [iOS simulator](https://docs.expo.dev/workflow/ios-simulator/)
- [Expo Go](https://expo.dev/go) (limited sandbox)

## Project structure

```
src/            # Application source code
app/            # Expo Router file-based routes
assets/         # Static assets (images, fonts)
scripts/        # Utility scripts
```

## Environment variables

Configuration is loaded via `app.json` extras or a `.env` file with
`expo-constants`.

| Variable  | Description                         | Default                  |
| --------- | ----------------------------------- | ------------------------ |
| `API_URL` | Base URL of the ASP.NET backend     | `http://localhost:5000`  |
| `WS_URL`  | WebSocket URL for real-time updates | `ws://localhost:5000/ws` |

## Related repositories

- **[kuvox-frontend](../frontend)** — React web frontend
- **[kuvox-api](../api)** — ASP.NET business backend
- **[kuvox-ai](../ai-service)** — Python AI / media service
