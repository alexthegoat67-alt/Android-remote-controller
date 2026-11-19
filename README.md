# iPhone Duo Remote Controller

A web-based remote control system that mirrors an unfolded iPhone Duo (`2670 x 1878` / `1.42:1` aspect ratio) to a GitHub Pages website and uses a Raspberry Pi 5 + XY stepper motor gantry + grounded capacitive stylus to physically tap the screen from anywhere over Wi-Fi or cellular.

## Current Progress
- **Frontend (`index.html`):** Live on GitHub Pages (`https://github.io`). Includes responsive `2670/1878` unfolded screen sizing, zero-delay iPad `pointerdown` touch detection (`0%–100%`), visual red tap indicator, and a frosted-glass password lock screen.
- **Hardware Planned:** Raspberry Pi 5 (4GB) with official 27W USB-C power supply & active cooler, XY stepper motors + drivers, SG90 servo Z-tapper, 3D-printed overhead gantry, and a grounded capacitive stylus.

## Next Steps
1. Set up screen mirroring from the iPhone Duo to the Raspberry Pi 5 (HDMI capture card or AirPlay) and stream video into `#phone-screen`.
2. Write the Python WebSocket server on the Raspberry Pi 5 to verify `sessionPassword` and convert `(X%, Y%)` coordinates into stepper motor steps.
3. Expose the Pi server securely using a Cloudflare Tunnel (`wss://`).
