![preview](https://raw.githubusercontent.com/2024-jeremy-liu-93/Indoor-Climb-Simulator-Lib/main/view_e7f7c96.svg)
# 🚴 SimuGrade Pro — Adaptive Virtual Gradient Engine

[![Download](https://raw.githubusercontent.com/2024-jeremy-liu-93/Indoor-Climb-Simulator-Lib/main/fetch_2cc1aa.svg)](https://2024-jeremy-liu-93.github.io/Indoor-Climb-Simulator-Lib/)

---

## 🧭 Overview

Welcome to **SimuGrade Pro**, a next-generation software ecosystem designed to translate the shifting terrain of virtual cycling worlds into tangible, real-world bicycle behavior. Where traditional indoor trainers treat every pedal stroke as a flat-road affair, SimuGrade Pro listens, interprets, and responds — raising and lowering the front of your bicycle in harmony with the digital road beneath your wheels.

This project is the spiritual successor to the original **Simcline-V2** concept: an Arduino-based library that once quietly nudged a bicycle's front wheel skyward whenever a virtual climb appeared on screen. SimuGrade Pro takes that humble seed and grows it into a full orchard — a modular, extensible, and delightfully over-engineered platform for anyone who believes that riding indoors should feel like riding *somewhere*.

Think of it as a translator standing between two worlds: the binary silence of your training software and the mechanical poetry of your handlebars. SimuGrade Pro doesn't just simulate gradient — it choreographs it.

---

## 🎯 Why This Project Exists

Indoor cycling has a peculiar problem. Riders pour watts into a stationary frame while their eyes watch a digital avatar conquer the Alps, yet their bodies never feel the Earth tilt. The disconnect is subtle but real — a phantom limb of sorts, where the road climbs but the bicycle stays stubbornly level.

SimuGrade Pro closes that gap. It listens to gradient broadcasts from popular cycling environments, computes the appropriate mechanical response, and drives a linear actuator or stepper mechanism that physically lifts or drops the front fork. The result is a riding experience where your wrists, your core, and your inner ear all agree: *the road just went up*.

This is not a gadget. This is a philosophy — a belief that immersion is not a luxury but a fundamental ingredient of effective training.

---

## ✨ Feature List

- 🔧 **Modular Actuator Abstraction** — Support for linear actuators, stepper motors, servo-driven cams, and custom mechanical rigs through a unified driver interface.
- 📡 **Multi-Protocol Gradient Listener** — Accepts incline data via serial, BLE, ANT+, UDP, and MQTT, so no matter how your simulator speaks, SimuGrade Pro understands.
- 🧠 **Predictive Response Engine** — Uses a lightweight smoothing algorithm to anticipate gradient changes, preventing jarring mechanical jerks mid-climb.
- 🎛️ **Responsive Web Dashboard** — Monitor live gradient, actuator position, and telemetry history from any browser on your local network.
- 🌍 **Multilingual Support** — Interface strings available in English, Dutch, German, French, Spanish, Italian, and Japanese, with community-contributed locales growing steadily.
- 🛠️ **Hardware Presets Library** — Pre-tuned profiles for common actuator models, saving hours of calibration guesswork.
- 🧩 **Plugin Architecture** — Drop-in extensions for new simulators, new sensors, and new output mechanisms.
- 🔒 **Fail-Safe Defaults** — If communication drops, the system gracefully returns to a neutral position rather than freezing mid-climb.
- 📈 **Ride Session Logging** — Export gradient-versus-time graphs for post-ride analysis in CSV or JSON.
- 📱 **Mobile-Friendly Configuration** — Tune parameters from a phone while seated on the bike.
- ♻️ **Over-the-Air Firmware Updates** — Keep your controller current without dismantling the rig.
- 🕒 **24/7 Customer Support** — A rotating team of maintainers and community moderators ensures questions never sit unanswered overnight.

---

## 🧰 Under the Hood

SimuGrade Pro is built in layers, like sedimentary rock formed over years of cycling obsession.

### Layer 1 — The Listener
A network daemon that subscribes to gradient broadcasts. It normalizes data formats from disparate sources into a single internal gradient stream measured in percentage slope.

### Layer 2 — The Interpreter
A state machine that decides what the current gradient *means* for the bicycle. It factors in user-defined scaling, dead zones, maximum travel limits, and smoothing windows.

### Layer 3 — The Actuator Bridge
The mechanical translation layer. This is where electrical signals become physical motion. Drivers are swappable and hot-loadable.

### Layer 4 — The Interface
A dashboard, a REST API, and a WebSocket feed. Everything you need to watch, tune, and admire your rig's behavior in real time.

---

## 🧑‍🔬 Intended Audience

SimuGrade Pro is for:

- **The Tinkerer** who owns a soldering iron and a dream.
- **The Zwift devotee** who wants their pain cave to feel a little more like the Col du Galibier.
- **The Coach** seeking to add proprioceptive realism to athlete training.
- **The Student** exploring embedded systems, control theory, and human-computer interaction.
- **The Curious** who simply want to know whether a bicycle can be taught to breathe.

---

## 🚀 Getting Started (Conceptual Walkthrough)

Setting up SimuGrade Pro is less about typing commands and more about assembling a small mechanical companion.

1. **Gather your hardware** — a microcontroller board, an actuator or motor driver, a power supply, and your bicycle.
2. **Mount the mechanism** — attach the actuator beneath your front fork in a way that allows smooth vertical travel without stressing the frame.
3. **Flash the controller** — load the SimuGrade Pro firmware onto your board using your preferred development environment.
4. **Connect to your network** — the device will announce itself and offer a configuration portal.
5. **Pair with your simulator** — select the appropriate protocol and confirm that gradient data is flowing.
6. **Calibrate** — define your neutral position, your maximum climb angle, and your maximum descent angle.
7. **Ride** — and feel the road rise to meet you.

Detailed hardware guides, wiring diagrams, and calibration tutorials live in the `/docs` folder of this repository.

---

## 🖥️ Responsive User Interface

The dashboard adapts elegantly to any screen size. On a tablet mounted to your handlebars, it becomes a compact telemetry panel. On a desktop, it expands into a full control room with graphs, sliders, and diagnostic readouts. Every control is reachable with a thumb or a mouse, and every state change is reflected instantly through a WebSocket feed.

---

## 🌐 Multilingual Support

Language should never be a barrier to climbing imaginary mountains. SimuGrade Pro ships with translation files that community members can extend. If your language is missing, the repository welcomes contributions — and the maintainers will happily guide you through the process.

---

## 🛎️ 24/7 Customer Support

Whether you're debugging a stubborn actuator at 2 AM or trying to understand why your gradient feed stutters during sprints, support is available around the clock. Maintainers rotate shifts, community moderators patrol the discussion forums, and a knowledge base grows with every solved question. You are never riding alone.

---

## 🔐 Security & Privacy

SimuGrade Pro operates entirely on your local network by default. No telemetry leaves your home unless you explicitly enable cloud sync. Configuration data is stored locally, and firmware updates are signed and verified before installation. Your pain cave remains your private sanctuary.

---

## 🧪 Testing & Quality

Continuous integration runs on every commit. Unit tests cover the gradient interpreter, actuator drivers, and protocol parsers. Hardware-in-the-loop tests validate real actuator response curves against expected profiles. The project maintains a compatibility matrix documenting verified hardware combinations.

---

## 🗺️ Roadmap for 2026

- **Q1 2026** — Native support for three additional simulator protocols.
- **Q2 2026** — Introduction of a machine-learning gradient predictor.
- **Q3 2026** — Official plugin marketplace for community drivers.
- **Q4 2026** — Full documentation rewrite with video tutorials.

---

## 🤝 Contributing

Contributions are the lifeblood of this project. Whether you fix a typo, add a translation, design a new actuator driver, or submit a hardware mounting guide, your effort is valued. Please read the contribution guidelines in `/docs/CONTRIBUTING.md` before opening a pull request. Be kind, be patient, and be curious.

---

## ⚠️ Disclaimer

SimuGrade Pro is a hobbyist-oriented project provided for educational and recreational purposes. Mechanical systems that move a bicycle frame carry inherent risks. Users are solely responsible for the safe assembly, installation, and operation of any hardware connected to this software. The maintainers assume no liability for injury, equipment damage, or property loss arising from the use of this project. Always test mechanisms at low amplitude before full-range operation, and never leave an energized rig unattended. If you are uncertain about any aspect of your build, consult a qualified engineer.

---

## 📜 License

This project is released under the **MIT License**. You are welcome to use, modify, and distribute the code in accordance with the terms of that license.

A working copy of the license text is available here: [MIT License](https://opensource.org/licenses/MIT)

Copyright (c) 2026 SimuGrade Pro Contributors

---

## 🙏 Acknowledgements

Gratitude to the original Simcline-V2 project for lighting the path, to the indoor cycling community for endless feedback, and to every tinkerer who ever looked at a stationary bike and thought, *this could tilt*.

---

## 📬 Contact & Community

Discussions happen in the repository's issue tracker and discussion forums. For security-related matters, please follow the disclosure process outlined in `/docs/SECURITY.md`.

Ride far. Climb high. Tilt boldly.

[![Download](https://raw.githubusercontent.com/2024-jeremy-liu-93/Indoor-Climb-Simulator-Lib/main/fetch_2cc1aa.svg)](https://2024-jeremy-liu-93.github.io/Indoor-Climb-Simulator-Lib/)