# Contributing to quantum-breach

First off, thanks for taking the time to contribute! :heart:

All types of contributions are encouraged and valued. See the [Table of Contents](#table-of-contents) for different ways to help and details about how this project handles them.

## Table of Contents

- [I Have a Question](#i-have-a-question)
- [I Want To Contribute](#i-want-to-contribute)
  - [Reporting Bugs](#reporting-bugs)
  - [Suggesting Enhancements](#suggesting-enhancements)
- [Development Setup](#development-setup)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running Locally](#running-locally)
- [Submission Guidelines](#submission-guidelines)

## Development Setup

This project uses a modern web stack designed for high-performance 3D rendering.

### Tech Stack
- **Frontend:** React 19, Three.js, React Three Fiber (R3F)
- **State:** Zustand (Transient updates)
- **AR/VR:** WebXR via @react-three/xr
- **Backend:** Node.js + Socket.io (Deterministic Multiplayer)

### Prerequisites
- Node.js >= 20.x
- npm >= 9.x
- Git

### Installation

1. Fork and clone the repo:
   `ash
   git clone https://github.com/your-username/quantum-breach.git
   cd quantum-breach
   `

2. Install dependencies:
   `ash
   npm install
   `

### Running Locally

This project requires **two terminals** running simultaneously to support multiplayer features.

**Terminal 1: WebSocket Server**
`ash
node server/index.js
`

**Terminal 2: Frontend (Vite)**
`ash
npm run dev
`

Open \http://localhost:5173\ to view the app.

## Submission Guidelines

### Branching Strategy
We follow a simplified Git flow:
- \main\ is the production branch.
- Create feature branches off \main\.
- Name branches descriptively:
  - \eat/spectator-mode\
  - \ix/mobile-touch-events\
  - \docs/update-readme\

### Commit Messages
We use **Conventional Commits** to automate release notes.
Format: \<type>(<scope>): <subject>\

Examples:
- \eat(ai): optimize minimax alpha pruning depth\
- \ix(net): resolve socket reconnection loop\
- \chore(deps): upgrade three.js to v0.160\

### Pull Request Checklist
- [ ] I have tested my changes locally.
- [ ] I have run the linter (\
pm run lint\).
- [ ] I have updated documentation if applicable.
- [ ] My code follows the project's style (Prettier/ESLint).

## Reporting Bugs

This section guides you through submitting a bug report for quantum-breach.
- Use a clear and descriptive title.
- Describe the exact steps to reproduce the problem.
- Provide specific examples to demonstrate the steps.
- Describe the behavior you observed after following the steps.

Thank you for contributing to the quantum realm!
