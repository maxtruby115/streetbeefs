# Street Beefs

A retro 90s pixel-art fighting game that runs in the browser. Made for phones (landscape) and works with a keyboard too.

- Static site: `index.html` plus `music/` and `voice/`. No build step.
- Deploy: import this repo into Vercel with the default settings (Framework Preset: Other). Every push to `main` redeploys.
- Online: ONLINE mode connects two devices peer-to-peer with a 4-letter room code (PeerJS, `lib/peerjs.min.js`, free public broker for the handshake only).
  - Lockstep netcode: both devices run the same simulation from exchanged inputs with a small input delay sized from ping.
  - The host sends a state check every 1.5s; if the guest has drifted, it reloads the host's state and replays.
  - Local testing: run a PeerJS server and open `index.html?peerhost=127.0.0.1&peerport=9000&peerpath=/`.
