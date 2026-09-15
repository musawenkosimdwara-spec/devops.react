# DEVCORE Mobile

React Native (Expo + TypeScript) mobile frontend for DEVCORE. Includes customer browsing/cart/checkout and an admin dashboard.

## Setup

```bash
npm install
```

You'll also need:

```bash
npx expo install @react-native-async-storage/async-storage @react-native-picker/picker
```

Fonts referenced in `src/styles/typography.ts` (`CormorantGaramond_500Medium`, `DMSans_400Regular`, `DMSans_700Bold`, `DMSans_600SemiBold`) need to be loaded via `expo-font` / `@expo-google-fonts` in `App.tsx`, or swapped for the closest Google Fonts packages:

```bash
npx expo install @expo-google-fonts/cormorant-garamond @expo-google-fonts/dm-sans expo-app-loading
```

## Backend

Point `API_URL` in `.env` at your Express backend. Defaults to `http://10.0.2.2:5000/api` (Android emulator loopback). For iOS simulator or a physical device, use your machine's LAN IP instead, e.g. `http://192.168.1.x:5000/api`.

## Run

```bash
npx expo start
```

Scan the QR code with Expo Go, or press `a` / `i` for an emulator/simulator.

## Notes on this build

- All `.ts`/`.tsx` files have been syntax-validated with a Babel (TypeScript + React) transform.
- `src/services/*`, `src/context/ProductFilterContext.tsx`, `src/screens/Auth/*`, `src/components/CartItem.tsx`, `SearchBar.tsx`, `CategoryChips.tsx`, and the `common/` components were filled in to complete the app end-to-end, matching the interfaces implied by the screens.
- `assets/fonts` and `assets/images` are empty placeholders — drop your font files and product/logo images in there.
