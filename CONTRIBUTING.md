# Contributing to quantum-breach-webxr

Thank you for your interest! This is a high-performance WebXR strategy game
built with React Three Fiber, TypeScript, and Socket.io. Contributions that
improve the AI, rendering performance, or multiplayer reliability are welcome.

## Prerequisites

- **Node.js v18+**
- **npm** or **yarn**
- A WebXR-compatible browser (Chrome on Android for AR mode)

## Local Development Setup

This project requires two terminals running simultaneously:

**Terminal 1 — WebSocket Server:**
```
node server/index.js
```

**Terminal 2 — React Frontend:**
```
npm install
npm run dev
```

Then open `http://localhost:5173` in your browser.

## What to Contribute

- 🤖 **AI improvements** — deeper Minimax search, better heuristics
- 🌐 **Multiplayer stability** — edge cases in deterministic sync
- 📱 **WebXR / AR enhancements** — surface detection, device compatibility
- ⚡ **Performance** — render loop optimizations, draw call reduction
- 🐛 **Bug fixes** — especially cross-browser or mobile issues

## Code Style

- **TypeScript strict mode** is enforced — no `any` types.
- Use **functional React components** with hooks only.
- State management is handled exclusively via **Zustand** — do not introduce
  additional state libraries.
- For render-critical state (animations), use Zustand **transient updates**
  (`subscribe`) to bypass React's render cycle.
- Follow the existing file structure: game logic in `src/game/`,
  components in `src/components/`, the AI worker in `src/workers/`.

## Commit Convention

We follow [Conventional Commits](https://www.conventionalcommits.org/):
- `feat:` New feature
- `fix:` Bug fix
- `perf:` Performance improvement
- `docs:` Documentation only
- `refactor:` Code restructuring

## Pull Request Checklist

- [ ] `npm run build` completes without errors or TypeScript warnings
- [ ] Tested in both Single Player and Multiplayer modes
- [ ] No regressions in 60FPS rendering on a mid-range device
- [ ] (If AR-related) Tested on a physical WebXR-compatible device
