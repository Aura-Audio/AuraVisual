# AuraVisual

## Overview

AuraVisual is a proprietary framework and SaaS platform that translates audio properties — frequency, amplitude, timbre, rhythm, and spatial positioning — into predictable, repeatable visual representations. Unlike generative visualizers that produce random output, AuraVisual operates on a **common design language**: a deterministic rule set that ensures every user, on every device, receives the exact same visual experience from the same audio input.

**Core Philosophy:**
- **Systematic over Stochastic:** Mapping rules are codified, versioned, and testable — not left to algorithmic chance.
- **Safety by Design:** Built-in WCAG 2.3.1 / ISO 9241-391 compliance guards against photosensitive seizure triggers.
- **Universal Accessibility:** Zero specialized hardware required. Runs in any browser, on any screen, with any speaker or headphone setup.
- **Cross-Modal Integrity:** Audio and visual remain tightly coupled without inducing sensory overload, threshold erosion, or perceptual disturbance.

**Target Use Cases:**
- Music streaming platforms (artist-branded visualizers)
- Live event LED/projection systems
- Game engine environmental audio-reactive effects
- Broadcast and podcast graphics automation
- Corporate event branding and experiential marketing
- Wellness / guided meditation apps requiring therapeutic reliability

---

## Features

### Core Framework
| Feature | Description |
|---------|-------------|
| **Deterministic Mapping Engine** | Same audio input + same mapping rule = identical visual output. Enables brand consistency, therapeutic reliability, and pre-flight safety analysis. |
| **Multi-Renderer Architecture** | WebGL 2.0, Canvas 2D, and SVG backends with automatic fallback based on device capability and power profile. |
| **Real-Time & Offline Modes** | Stream visuals live from microphone/line-in, or batch-process audio files for pre-rendered export (MP4, WebM, image sequence). |
| **Cross-Platform SDK** | Native plugins for Unity, Unreal Engine, and Web Audio API. Embed AuraVisual into games, DAWs, or mobile apps. |
| **Cloud-Native API** | RESTful and WebSocket APIs for SaaS integration. Server-side execution keeps proprietary mapping logic secure. |

### Safety & Compliance
| Feature | Description |
|---------|-------------|
| **WCAG 2.3.1 Flash Governor** | Hard-coded engine-level enforcement: no visual transition exceeds 3 flashes per second. Red-flash and luminance-delta filters applied automatically. |
| **Pre-Flight Hazard Analysis** | Scan any audio file before rendering to flag sections that would violate safety thresholds (e.g., drum solos >180 BPM mapped to full-screen flashes). |
| **Health-Safe Presets** | One-click modes: Epilepsy-Safe, VSS/Migraine-Safe, Sensory-Reduced, and Pediatric. Each constrains contrast, motion, color temperature, and transition speed. |
| **Session Governance** | Configurable auto-pause timers, volume normalization (≤85 dB SPL), and ambient light detection advisories. |

### Enterprise & Creator Tools
| Feature | Description |
|---------|-------------|
| **Visual Style Marketplace** | Community and premium "mapping packs" — reusable rule sets for genres, brands, or therapeutic protocols. Revenue-share model for creators. |
| **White-Label Enterprise** | Self-hosted or private-cloud deployments with SSO (SAML/OIDC), audit logs, and SLA guarantees. |
| **Brand Kit Integration** | Lock color palettes, typography, and motion language to corporate identity guidelines. |
| **Analytics Dashboard** | Usage telemetry, safety event logging, and API throughput metrics. |

---

## Project Structure

```

AuraVisual/
├── README.md                      # This file
├── OVERVIEW.md                    # High-level system architecture & design principles
│
├── docs/
│   ├── 01-protection.md           # IP, trade secret, and legal protection strategy
│   ├── 02-business-plan.md        # 5-year roadmap, market sizing, pricing tiers
│   ├── 03-comparison.md           # Comparative analysis vs. AR/VR and adjacent tech
│   └── 04-health-and-safety.md    # Clinical risk assessment, WCAG compliance, medical disclaimers
│
├── src/
│   ├── core/
│   │   ├── engine/                # Deterministic mapping engine (audio feature extraction → visual rule application)
│   │   ├── rules/                 # Built-in mapping rule definitions (bass→expansion, treble→shimmer, etc.)
│   │   └── safety/                # Flash-rate governor, luminance caps, pre-flight analyzer
│   │
│   ├── renderers/
│   │   ├── webgl/                 # WebGL 2.0 fragment shaders for high-performance visualization
│   │   ├── canvas2d/              # Canvas 2D fallback for low-power devices
│   │   └── svg/                   # Vector output for broadcast/post-production pipelines
│   │
│   ├── api/
│   │   ├── rest/                  # RESTful endpoints (upload audio, retrieve rendered frames)
│   │   ├── websocket/             # Real-time streaming API
│   │   └── sdk/                   # Client libraries (JS, Python, C#)
│   │
│   └── plugins/
│       ├── unity/                 # Unity Asset Store package
│       ├── unreal/                # Unreal Engine plugin
│       └── ableton/               # Max for Live device (future)
│
├── assets/
│   ├── branding/                  # Logos, wordmarks, social assets
│   ├── templates/                 # Default visual style templates (JSON rule sets)
│   └── demo-media/                # Sample audio clips for testing and demo reels
│
├── tests/
│   ├── unit/                      # Engine and renderer unit tests
│   ├── integration/               # API and SDK integration tests
│   ├── safety/                    # WCAG 2.3.1 compliance test suite (automated flash-rate validation)
│   └── fixtures/                  # Audio test fixtures (sine sweeps, BPM grids, white noise)
│
├── scripts/
│   ├── build/                     # Cross-platform build scripts
│   ├── deploy/                    # Cloudflare Pages / Docker deployment helpers
│   └── lint/                      # Code quality and safety rule linting
│
├── .github/
│   ├── workflows/                 # CI/CD: test → safety audit → build → deploy
│   └── ISSUE_TEMPLATE/            # Bug reports, feature requests, safety incident reports
│
├── LICENSE                        # Proprietary license (see docs/01-protection.md)
└── package.json / Cargo.toml / pyproject.toml  # Multi-language manifest (JS frontend, Rust core, Python SDK)

```

---

## Documentation

All strategic, legal, and technical reference documents are maintained in the `docs/` directory:

| Document | Contents |
|----------|----------|
| [`docs/01-protection.md`](docs/01-protection.md) | IP strategy: trade secrets, copyright, patent positioning, trademark, and anti-theft technical measures. |
| [`docs/02-business-plan.md`](docs/02-business-plan.md) | 5-year financial roadmap, TAM/SAM/SOM metrics for English-language markets, pricing tiers, and target customer segments. |
| [`docs/03-comparison.md`](docs/03-comparison.md) | Head-to-head analysis against AR, VR, spatial audio, and traditional video — covering features, compliance, health & safety, and product fit. |
| [`docs/04-health-and-safety.md`](docs/04-health-and-safety.md) | Clinical risk assessment: photosensitive epilepsy, visual snow syndrome, migraine triggers, auditory hallucination theory, and mandatory technical safeguards. |

---

## Roadmap

### Phase 1: Foundation (Year 1)
- [x] Core deterministic mapping engine (v0.1)
- [x] WebGL 2.0 + Canvas 2D dual renderer
- [x] WCAG 2.3.1 flash-rate governor and pre-flight analyzer
- [x] Cloud SaaS MVP with freemium tiers
- [ ] REST API v1 (Q3)
- [ ] JavaScript SDK + embeddable widget (Q3)
- [ ] First enterprise pilot (Q4)

### Phase 2: Platform & Integration (Year 2)
- [ ] Unity and Unreal Engine SDKs
- [ ] WebSocket real-time streaming API
- [ ] Visual Style Marketplace (community rule packs)
- [ ] SOC 2 Type II certification
- [ ] US entity establishment (Delaware C-Corp)
- [ ] White-label enterprise tier (self-hosted appliance)

### Phase 3: Scale & Ecosystem (Year 3)
- [ ] AI-assisted mapping rule generation (human-in-the-loop)
- [ ] Broadcast integration (NDI / SDI output for live TV)
- [ ] Plugin ecosystem (DAW VST, OBS Studio, TouchDesigner)
- [ ] Open standard working group (subset protocol publication)
- [ ] Australia / NZ market entry

### Phase 4: Vertical Dominance (Year 4)
- [ ] Hardware partnerships (LED controller OEM integration)
- [ ] Medical/wellness vertical (FDA/EMA consultation for therapeutic claims)
- [ ] Mobile native apps (iOS / Android) with offline rendering
- [ ] Advanced analytics and A/B testing for mapping rule performance

### Phase 5: Category Standard (Year 5)
- [ ] Published open standard for audio-visual design languages
- [ ] Certification program ("Certified AuraVisual Designer")
- [ ] Strategic partnership or acquisition discussions
- [ ] Dublin + London + New York team presence
- [ ] v5.0 — autonomous real-time adaptive mapping based on biometric feedback (opt-in)

---

## Health & Safety

⚠️ **AuraVisual is an audio-visual stimulation system. Before use, please review [`docs/04-health-and-safety.md`](docs/04-health-and-safety.md).**

- **Photosensitive Epilepsy:** All default templates comply with WCAG 2.3.1 (Level A). Users can enable WCAG 2.3.2 (AAA) "Maximum Safety" mode.
- **Session Limits:** Health-safe presets enforce auto-pause timers. Users with migraine, visual snow, or sensory processing conditions should start with "Sensory-Reduced" mode.
- **Medical Disclaimer:** AuraVisual is not a medical device. Therapeutic use cases require independent clinical validation and regulatory consultation.
- **Incident Reporting:** If you experience adverse effects (nausea, visual disturbances, headache), discontinue use immediately and file a safety incident via GitHub Issues.

---

## Quick Start

```bash
# Clone the repository
git clone https://github.com/Aura-Audio/AuraVisual.git
cd AuraVisual

# Install dependencies
npm install

# Run the development server (includes safety linting)
npm run dev

# Run the full test suite including WCAG compliance checks
npm run test:safety

# Build for production
npm run build
```

API Example

```javascript
import { AuraVisual } from '@auravisual/sdk';

const session = new AuraVisual({
  apiKey: 'YOUR_API_KEY',
  safetyMode: 'wcag-aaa', // 'default' | 'wcag-aaa' | 'vss-safe' | 'pediatric'
  renderer: 'webgl'
});

// Render visuals from an audio file
const visualStream = await session.render({
  audioUrl: 'https://example.com/track.mp3',
  mappingRule: 'aurora-bass-expansion-v2',
  outputFormat: 'mp4'
});

visualStream.pipe(fs.createWriteStream('output.mp4'));
```

---

Contributing

AuraVisual is currently proprietary software under active development. See [`docs/01-protection.md`](docs/01-protection.md) for IP and licensing terms.

- Bug Reports & Safety Issues: Please use [GitHub Issues](https://github.com/Aura-Audio/AuraVisual/issues) with the `safety-critical` label where applicable.
- Feature Requests: Open a discussion in [GitHub Discussions](https://github.com/Aura-Audio/AuraVisual/discussions).
- Enterprise Inquiries: Contact `enterprise@auravisual.audio`

---

License

© 2026 AuraVisual. All rights reserved.

This repository and its contents are proprietary and confidential. Unauthorized copying, distribution, or reverse engineering is strictly prohibited. See `LICENSE` and `docs/01-protection.md` for full terms.
