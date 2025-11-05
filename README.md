# Browser-Only Peer-to-Peer Chat Demo (WebRTC)

This is a **simple, browser-only demonstration** of peer-to-peer (P2P) chat using **WebRTC**. It allows two users to connect directly from their browsers and exchange messages without a central server, using STUN/TURN servers to traverse NATs and firewalls.

---

## Features

- **P2P chat between 2 browsers** – no backend required
- **Manual SDP exchange** – copy-paste Session Description Protocol (SDP) text to establish a connection
- **TURN mode support** – use public TURN servers to bypass restrictive networks
- **Status toasts** – visual feedback for connection events
- **ICE candidate logging** – inspect connection attempts and candidates in real-time

---

## How to Use

1. Open the HTML file in **two different browsers or tabs**.
2. On the 1st browser, click **Create Offer**. The local SDP will be automatically copied to the clipboard.
3. On the 2nd browser **Paste and Generate** the local SDP from the first browser, which will generate an answer.
4. On the 1st browser **Paste Offer & Connect** the local SDP from the second browser's answer.
5. Once both peers have exchanged SDPs, the **DataChannel opens**, and you can send chat messages.

## TURN Modes

The demo includes a **TURN mode toggle**:

1. **STUN (fast)** – only uses a public STUN server for fast connections; may fail behind strict NATs.
2. **STUN/TURN (fast & slow - reliable)** – tries STUN first, falls back to TURN if needed.
3. **Force TURN Only (slow & reliable)** – forces all connections through TURN for maximum reliability.

**Public TURN servers included**:

```json
{
  "urls": [
    "turn:openrelay.metered.ca:80",
    "turn:openrelay.metered.ca:443",
    "turns:openrelay.metered.ca:443"
  ],
  "username": "openrelayproject",
  "credential": "openrelayproject"
}
```


## HelloWorld Demos
To help you navigate, here's a complete list of my hello world demos

### Simple Demos
- 2D SVG - [helloworld_html_js_svg](https://github.com/subatomicglue/helloworld_html_js_svg)
- 2D Canvas - [helloworld_html_js_canvas](https://github.com/subatomicglue/helloworld_html_js_canvas)
- 3D Canvas - [threejs-helloworld-cube](https://github.com/subatomicglue/threejs-helloworld-cube)
- 2D Spline Curve through points - [helloworld-catmull-rom-spline-curve](https://github.com/subatomicglue/helloworld-catmull-rom-spline-curve)

### More Advanced Demos
- 2D Canvas with fractal tree - [fractaltree](https://github.com/subatomicglue/fractaltree)
- 2D Canvas with sprites and map tiles - [sprite_demo_js](https://github.com/subatomicglue/sprite_demo_js)
- Audio Demo with drummachine - [drummachine](https://github.com/subatomicglue/drummachine)
- Audio Demos:  MIDI music, Audio player - [drummachine](https://github.com/subatomicglue/kiosk)
- Peer to Peer chat using WebRTC - [helloworld_html_js_webrtc_p2p](https://github.com/subatomicglue/helloworld_html_js_webrtc_p2p)

