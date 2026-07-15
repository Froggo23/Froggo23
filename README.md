<!-- Banner-style header -->
<div align="center">

  <!-- typing-style title -->
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=3200&pause=900&color=3DD68C&center=true&vCenter=true&width=650&lines=Hey%2C+I'm+Ian+Choe+%F0%9F%90%B8;I+turn+the+body+into+an+input+device;webcam+%E2%86%92+Vision+%E2%86%92+gestures+%E2%86%92+control" alt="Typing SVG" />

  <p>
    <strong>Froggo23</strong> · high-school builder of native macOS interfaces<br/>
    Swift · Apple Vision · AVFoundation · a healthy amount of Spring Boot
  </p>

  <p>
    <a href="https://github.com/Froggo23">
      <img src="https://img.shields.io/badge/GitHub-Froggo23-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
    </a>
    <a href="https://www.linkedin.com/in/ian-choe-9615503a1/">
      <img src="https://img.shields.io/badge/LinkedIn-Ian_Choe-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn" />
    </a>
    <a href="https://www.instagram.com/ianchoe09/">
      <img src="https://img.shields.io/badge/Instagram-ianchoe09-E4405F?style=for-the-badge&logo=instagram&logoColor=white" alt="Instagram" />
    </a>
    <a href="mailto:toponfrog23@gmail.com">
      <img src="https://img.shields.io/badge/Email-toponfrog23-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email" />
    </a>
  </p>
</div>

---

### 👋 About me

I'm a high-school student who builds **embodied HCI prototypes**: native macOS apps that read your body through the webcam and turn it into a controller — for games, for the keyboard, for a synthesizer. Everything below is a personal project, written to learn how these systems actually work under the hood. No web wrappers; just Apple frameworks, `CGEvent` taps, and hand-tuned thresholds.

Also: yes, I like frogs. 🐸

---

### ✨ Featured — the macOS body-control trilogy

Three Swift apps (~4,400 lines total) built on the same idea: camera in, Vision framework in the middle, synthetic input or audio out.

**🥊 [mac-boxing-body-control](https://github.com/Froggo23/mac-boxing-body-control)** — Play games by boxing at your webcam. An `AVCaptureSession` streams frames (~30 fps) into Vision's `VNDetectHumanBodyPoseRequest`; a gesture state machine compares each frame's joint geometry against a 14-frame calibrated neutral stance and classifies punches, guard, ducks, and leans using hand-tuned angle/distance thresholds with hysteresis and cooldowns. Recognized gestures become synthetic keyboard/mouse events via `CGEvent` posted to the HID event tap (needs Accessibility permission). A floating AppKit debug window shows the mirrored feed with skeleton overlay, neutral-pose crosshair, and live key readout.

**🖐️ [mac-finger-game-control](https://github.com/Froggo23/mac-finger-game-control)** — WASD, but it's your fingers. A single-file Swift app runs Vision's `VNDetectHumanHandPoseRequest` on webcam frames and classifies finger folds, thumb pinches, fists, and an open-hand stop from joint distances normalized by palm size. Gestures translate into HID-level `CGEvent` key-down/key-up events — W/A/S/D holds plus Space/E/I/O taps with cooldowns. An AppKit debug window overlays the hand skeleton, per-fingertip key badges, and gesture state.

**🎛️ [mac-hand-vocoder](https://github.com/Froggo23/mac-hand-vocoder)** — Your hand is the synth patch. Per-finger bend states (from hand-pose joint distances), hand height, and finger spread are exponentially smoothed and mapped to DSP parameters. Mic audio flows from an `AVAudioEngine` input tap through a lock-guarded ring buffer into an `AVAudioSourceNode` running a hand-written vocoder-style effect: an envelope follower drives a three-oscillator carrier through three swept biquad band-pass "formant" filters, plus modulated-delay chorus and tanh soft clipping. One ~1,500-line Swift file, only Apple frameworks, compiled by a `swiftc` shell script into an ad-hoc-signed app bundle.

---

### 🧠 Currently building

A personal **second-brain agent** on the raw Anthropic API — hand-writing the agentic loop and tool use myself (no framework), adding retrieval over my own notes, then an MCP server and an eval harness. The goal is to learn how agent harnesses work by building one, in public. It lives (in progress) at `Froggo23/brain`.

---

### 🛠️ Also built

- **[rankmyart](https://github.com/Froggo23/rankmyart)** — art-ranking web app (Spring Boot, AWS S3, Docker/Jenkins), team project with [jnoh27](https://github.com/jnoh27)
- **[redscreen](https://github.com/Froggo23/redscreen)** — Chrome extension that tints distracting sites red to nudge me back to work
- **[frutiger-surfer](https://github.com/Froggo23/frutiger-surfer)** — Frutiger Aero / hopecore open-roam game; you are a blue figurine on a floating disc
- **[ratekis](https://github.com/Froggo23/ratekis)** — rate-my-teacher-style prototype for my school (KIS), Spring Boot + JPA with seeded demo data
- **[ensemble-live](https://github.com/Froggo23/ensemble-live)** — realtime ensemble room: Spring Boot + STOMP WebSockets, multiple people play a browser synth keyboard together

---

### 🧰 Tools I actually use

<p align="center">
  <img src="https://skillicons.dev/icons?i=swift,apple,java,spring,js,ts,py,html,css,git,github,vscode&perline=12" alt="Tech stack" />
</p>

<p align="center"><sub>Swift + Apple Vision/AVFoundation for the macOS work · Java/Spring for web backends · JS/TS and Python for everything else</sub></p>

---

<div align="center">
  <sub>Thanks for stopping by — go build something weird 🐸</sub>
</div>
