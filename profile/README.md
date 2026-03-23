<div align="center">

<img src="https://img.shields.io/badge/HTL%20St.%20P%C3%B6lten-Robotics-e63946?style=for-the-badge&logo=probot&logoColor=white" alt="HTL St. Pölten Robotics"/>

### Autonomous robotics · [HTL St. Pölten](https://www.htlstp.ac.at/) · Austria

Competing in [Botball](https://www.botball.org/) & [ECER](https://ecer.botball.org/)

*"Raise the Floor, Don't Lower the Ceiling"*

![C++](https://img.shields.io/badge/C%2B%2B20-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Dart](https://img.shields.io/badge/Dart%2FFlutter-02569B?style=flat-square&logo=flutter&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![C#](https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white)

</div>

---

## What We Do

We build autonomous robots that compete on a game table — navigating, detecting objects, and completing missions with zero human input. Our platform, **RaccoonOS**, is a full custom stack running on the [KIPR Wombat](https://www.kipr.org/kipr/hardware/botball-controller-wombat) controller, from bare-metal firmware up to a visual programming environment.

---

## RaccoonOS Architecture

Five layers, one shared LCM communication backbone — no capability gaps between beginner and expert workflows.

<div align="center">
  <img alt="RaccoonOS Architecture" src="https://raw.githubusercontent.com/htl-stp-ecer/.github/main/profile/architecture.svg" width="700"/>
</div>

---

## Quick Start

> 📖 Full documentation at **[docs.htl-stp-ecer.github.io](https://htl-stp-ecer.github.io/documentation)**

```bash
pip install raccoon-cli
raccoon init my-robot
raccoon hardware-wizard
```

- **New to the platform?** Start with the [Getting Started guide](https://htl-stp-ecer.github.io/documentation/getting-started).
- **Just want to read the code?** Start with [`raccoon-lib`](https://github.com/htl-stp-ecer/raccoon-lib) — it's the core.

---

## Repositories

### Core Platform

| Repository | Description | Tech |
|:-----------|:------------|:-----|
| **[raccoon-lib](https://github.com/htl-stp-ecer/raccoon-lib)** | Core robotics library — PID control, kinematics, odometry, step-based missions | ![C++](https://img.shields.io/badge/-C%2B%2B20-00599C?style=flat-square&logo=cplusplus&logoColor=white) ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) |
| **[stm32-data-reader](https://github.com/htl-stp-ecer/stm32-data-reader)** | Raspberry Pi ↔ STM32 SPI bridge, publishes sensor data via LCM | ![C++](https://img.shields.io/badge/-C%2B%2B20-00599C?style=flat-square&logo=cplusplus&logoColor=white) |
| **[raccoon-cli](https://github.com/htl-stp-ecer/raccoon-cli)** | Dev toolchain — scaffolding, hardware wizard, codegen, remote sync | ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) |
| **[botui](https://github.com/htl-stp-ecer/botui)** | StpVelox — Flutter desktop environment with real-time dashboard & sensor viz | ![Flutter](https://img.shields.io/badge/-Flutter-02569B?style=flat-square&logo=flutter&logoColor=white) |
| [WebIDE](https://github.com/htl-stp-ecer/WebIDE) | IDE | |
| **[raccoon-transport](https://github.com/htl-stp-ecer/raccoon-transport)** | LCM-based inter-process messaging (C++, Python, Dart) | ![C++](https://img.shields.io/badge/-C%2B%2B20-00599C?style=flat-square&logo=cplusplus&logoColor=white) ![Dart](https://img.shields.io/badge/-Dart-02569B?style=flat-square&logo=dart&logoColor=white) ![Python](https://img.shields.io/badge/-Python-3776AB?style=flat-square&logo=python&logoColor=white) |

### 📚 Documentation & Research

| Repository | Description |
|:-----------|:------------|
| **[documentation](https://github.com/htl-stp-ecer/documentation)** | Full platform docs — [hosted here](https://htl-stp-ecer.github.io/documentation) |
| **[Papers-and-Documentations](https://github.com/htl-stp-ecer/Papers-and-Documentations)** | ECER conference papers and competition archive |

---

## Origins

RaccoonOS grew out of **[Tobias Madlberger](https://github.com/ToberoCat)**'s years competing in Botball at HTL St. Pölten (2022–2026). What started as competition code went through multiple complete rewrites, slowly becoming a proper five-layer robotics platform - not by design, but by necessity.

The architecture, core libraries, firmware, and toolchain were all built from scratch, The platform was formally named *RaccoonOS* in September 2025.

On graduating in 2026, Tobias open-sourced everything — not just for future HTL teams, but for every Botball student who would otherwise face the same wall he hit in 2022: no documentation, no foundation, no starting point.

> *"Three years of figuring out what nobody wrote down - now it's written down."*

---

## Team

| Name | Role |
|:-----|:-----|
| **[Tobias Madlberger](https://github.com/ToberoCat)** | Founder & Lead Architect — platform design, middleware, firmware, toolchain, SDK, AI pipeline, WebIDE core, and everything in between (2022–2026, 1000+ hours) |
| Matthias Greil | Hardware & Firmware — STM32 implementation, IMU integration, low-level driver work; shaped the high-level SDK as a power user |
| Fabian Popov | AI & Visualization — object detection data labeling, game table visualization and simulation in the WebIDE |
| Jakob Schlögl | UI — BotUI development |
| Daniel Schneeweis | WebIDE — developed the web-based IDE |
| Florian Schwanzer | General Contributions — library work, sensor calibration, tests, and filling gaps wherever needed |
| Anna Theis | Early Adopter & Pre-Alpha Feedback — used the earliest bare-bones versions in real robot development, whose hands-on feedback shaped the foundation everything else grew from |

---

## Contributing

RaccoonOS is open to the wider Botball community.

- **Bug reports & feature requests** — open a GitHub issue in the relevant repo
- **Code contributions** — PRs welcome; see `CONTRIBUTING.md` in each repo
- **New teams** — reach out to senior teams as they have the knowlegde and can help you - alternatively read the docs

---

<div align="center">

![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-A22846?style=flat-square&logo=raspberrypi&logoColor=white)
![STM32](https://img.shields.io/badge/STM32-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![CMake](https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white)
![Unity](https://img.shields.io/badge/Unity-000000?style=flat-square&logo=unity&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)

**St. Pölten, Austria** · [htlstp.ac.at](https://www.htlstp.ac.at/)

</div>
