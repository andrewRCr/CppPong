# C++ Pong

Classic Pong built entirely from scratch in raw C++ — no game engine, no graphics API,
just direct pixel manipulation via Win32 GDI. Every system (renderer, game loop, collision
detection, entity architecture, menu state machine) is hand-rolled, organized into
distinct platform, framework, and game logic layers. Supports single-player against an
AI opponent and local two-player multiplayer, with 3D positional audio for spatialized
sound effects.

<p align="center">
  <a href="https://github.com/andrewRCr/CppPong/releases/latest">Download (Windows)</a>
  &nbsp;&nbsp;|&nbsp;&nbsp;
  <a href="https://andrewcreekmore.dev/projects/game/cpp-pong">Portfolio</a>
</p>

<div align="center">
  <a href="https://github.com/andrewcreekmore/Pong/assets/44483269/325ace15-94f4-4bff-bb7a-efd89411500c"><img src="https://github.com/andrewcreekmore/Pong/assets/44483269/325ace15-94f4-4bff-bb7a-efd89411500c" width="32%" alt="Main menu" /></a>
  <a href="https://github.com/andrewcreekmore/Pong/assets/44483269/0711f84c-70aa-4d23-8e5c-8a7267314304"><img src="https://github.com/andrewcreekmore/Pong/assets/44483269/0711f84c-70aa-4d23-8e5c-8a7267314304" width="32%" alt="Gameplay" /></a>
  <a href="https://github.com/andrewcreekmore/Pong/assets/44483269/6e1ac7e1-a671-48f4-a3d3-63b9dddd8ee5"><img src="https://github.com/andrewcreekmore/Pong/assets/44483269/6e1ac7e1-a671-48f4-a3d3-63b9dddd8ee5" width="32%" alt="Pause menu" /></a>
</div>

## Details

- Pure software rendering: direct pixel buffer writes to a VirtualAlloc framebuffer,
  blitted to screen via GDI StretchDIBits each frame
- 3D positional audio via OpenAL for spatialized gameplay sound effects
- Custom bitmap text rendering without font libraries
- Delta-timed game loop with AABB collision, paddle-velocity transfer, and state-driven
  pause
- Adaptive AI opponent with speed modulation and anti-stalemate logic
- Entity system with base class and Ball/Paddle specializations; state machine managing
  menu and gameplay transitions
- Local two-player multiplayer

## Technology

- **Language:** C++
- **Platform:** Win32 (GDI)
- **Audio:** OpenAL (openal-soft), libsndfile

## Controls

- **Single-player:** W/S or Up/Down to control the right paddle; compete against AI
- **Two-player:** W/S controls the left paddle, Up/Down controls the right paddle

<p align="center"><a href="#c-pong">↑ Back to top</a></p>
