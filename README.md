# Browser-Only Peer-to-Peer Chat Demo (WebRTC)

This is a **simple, browser-only demonstration** of peer-to-peer (P2P) chat using **WebRTC**. It allows two users to connect directly from their browsers and exchange messages without a central server, using STUN/TURN servers to traverse NATs and firewalls.

---

## Features

- **P2P chat in the browser** – no backend required
- **Manual SDP exchange** – copy-paste Session Description Protocol (SDP) text to establish a connection
- **TURN mode support** – use public TURN servers to bypass restrictive networks
- **Status toasts** – visual feedback for connection events
- **ICE candidate logging** – inspect connection attempts and candidates in real-time

---

## How to Use

1. Open the HTML file in **two different browsers or tabs**.
2. On one browser, click **Create Offer**. The local SDP will be automatically copied to the clipboard.
3. Paste the local SDP from the first browser into the **Remote SDP** textarea on the second browser and click **Paste Offer & Connect**.
4. The second browser will generate an answer; copy that SDP back to the first browser’s **Remote SDP** and paste it.
5. Once both peers have exchanged SDPs, the **DataChannel opens**, and you can send chat messages.

---

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
- Peer to Peer chat using WebRTC - [helloworld_html_js_webrtc_p2p](https://github.com/subatomicglue/helloworld_html_js_webrtc_p2p)

