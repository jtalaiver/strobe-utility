# Photic Strobe Utility

A zero-dependency, single-file web engine for testing photic driving and frequency-following response (FFR). This utility leverages a device's display to generate stroboscopic flicker, bypassing operating system hardware throttles on camera flashes to deliver frame-perfect neural entrainment frequencies.

## Architecture & Features

This project relies exclusively on vanilla HTML, CSS, and JavaScript. 

* **Frame-Synced Rendering:** Utilizes `requestAnimationFrame` to tie the strobe toggle directly to the device's screen refresh rate, preventing thread jitter and missed cycles.
* **EEG Frequency Mapping:** Presets target specific neurological states:
  * **6 Hz (Theta):** Deep calm / meditation.
  * **10 Hz (Alpha):** Relaxation / eyes-closed rest.
  * **18 Hz (Beta):** Active focus / alertness.
  * **40 Hz (Gamma):** Cognitive synchronization.
  * **2.5 Hz (Low Delta):** Sensory modulation.
* **Clinical Ramp Protocol:** Optional dynamic scaling that eases the user into the session. It initiates at a 15 Hz waking baseline, interpolates linearly down to the target frequency over the first 15% of the session, holds, and smoothly ascends back to baseline during the final 15% to prevent post-session fatigue.
* **Auto-Termination Timer:** Clinical standard session caps at 15, 20, or 30 minutes.
* **Mobile-Safe Fullscreen:** Implements defensive `try/catch` fallbacks to ensure the strobe loop executes even when mobile operating systems (like iOS Safari) reject asynchronous WebXR or standard fullscreen API requests.

## Deployment

Because the engine is entirely self-contained within `index.html`, deployment requires zero build steps or package managers.

1. Clone or download the repository.
2. Host the directory on GitHub Pages, Vercel, or any static file server.
3. Access the URL via a mobile device or desktop browser.

*Live Demo:* [joe.talaiver.com/strobe](https://joe.talaiver.com/strobe)

## Safety & Operational Warning

**Photosensitive Epilepsy Risk:** This utility generates rapid, high-contrast flashing lights. It must not be used by individuals with a personal or family history of epilepsy, seizures, or severe migraines. 

**Usage Protocol:** 
1. Activate "Do Not Disturb" on your device to prevent incoming notifications from breaking the visual loop.
2. Ensure device brightness is set to a comfortable level.
3. Close eyes before initiating the session. Photic driving is designed to operate through closed eyelids.
4. Tap the screen at any time