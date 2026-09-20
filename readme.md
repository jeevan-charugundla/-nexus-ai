# 🌌 NEXUS AI — Advanced Autonomous AI Assistant

![Nexus AI Banner](config/nexus.ico)

**Nexus AI** is a state-of-the-art, real-time autonomous multimodal desktop assistant powered by Google Gemini Live. Built with a sleek futuristic HUD interface, autonomous tool routing, proactive monitoring, vision processing, and an extensible drop-in plugin architecture.

---

## ✨ Features

- 🎙️ **Real-Time Voice & Multimodal Interaction**
  - Ultra-low latency voice communication via Gemini Live (`models/gemini-3.1-flash-live-preview`).
  - Native interruptibility, live waveform visualization, and dynamic state feedback.

- 🖥️ **Futuristic Sci-Fi HUD Interface**
  - Cyberpunk-inspired aesthetic with arc-reactor core visualization.
  - Live system telemetry (CPU, RAM, GPU, thermals) and interactive system drawer.
  - Floating clipboard companion for quick AI actions.

- 👁️ **Vision & Screen Understanding**
  - Real-time screen capture and webcam processing for visual reasoning and debugging.

- 💻 **OS & Computer Control**
  - Complete control over system volume, display brightness, Wi-Fi toggles, app launching, and shortcuts.
  - Safe confirmation gates for critical system actions.

- 🧠 **Persistent Long-Term Memory & Recall**
  - Automatically remembers user preferences, personal context, and past interactions.
  - Instant local recall search without roundtrips.

- 🤖 **Autonomous Dev Agent & Code Execution**
  - Builds full software projects from scratch directly on your desktop.
  - Interactive debugging and sandbox code runner.

- 📱 **Mobile Remote Control & Web Dashboard**
  - Secure QR-code pairing for mobile access over local network.
  - Web UI for sending commands, file transfers, and remote monitoring.

- 🧩 **Extensible Plugin Ecosystem**
  - Drop-in `.py` plugins in `plugins/` auto-discovered at boot with zero configuration.

---

## 🚀 Quick Start

### 1. Prerequisites
- Python 3.10+
- [Gemini API Key](https://aistudio.google.com/)

### 2. Installation
Clone the repository and install the dependencies:
```bash
git clone https://github.com/jeevan-charugundla/-nexus-ai.git
cd -nexus-ai
pip install -r requirements.txt
```

### 3. Running Nexus AI
```bash
python main.py
```

On first launch, the configuration setup drawer will prompt for your **Gemini API Key** and preferred assistant voice.

---

## 🛠️ Project Architecture

```
nexus-ai/
├── actions/                  # Auto-discovered modular tools & capabilities
│   ├── background_monitor.py # News & alert background polling
│   ├── browser_control.py    # Playwright browser automation
│   ├── code_helper.py        # Code snippet executor & debug tools
│   ├── computer_control.py   # Mouse, keyboard, and window management
│   ├── computer_settings.py  # OS brightness, audio, wifi control
│   ├── dev_agent.py          # Autonomous multi-file project builder
│   ├── file_processor.py     # Document reading & parsing
│   ├── screen_processor.py   # Screen & camera vision capture
│   └── system_monitor.py     # CPU / RAM / GPU metrics
├── core/                     # Core runtime infrastructure
│   ├── action_loader.py      # Dynamic tool registration
│   ├── audio_devices.py      # Input/output audio device selector
│   ├── installer.py          # On-demand dependency installer
│   ├── llm_client.py         # Gemini Live WebSocket protocol client
│   ├── plugin_loader.py      # Drop-in plugin engine
│   ├── prompt.txt            # Nexus AI core system instructions
│   └── wake_word.py          # OpenWakeWord local wake detection
├── dashboard/                # Remote HTTP & WebSocket companion server
├── memory/                   # Config and persistent memory engine
├── plugins/                  # Custom drop-in plugins
├── ui.py                     # PyQt6 HUD user interface
└── main.py                   # Main orchestration entrypoint
```

---

## ⚙️ Configuration & Customization

All settings can be adjusted via the in-app **Settings (⚙️)** drawer:
- **Assistant Name**: Default is `Nexus AI`.
- **Live Voice**: Choose between *Charon*, *Puck*, *Kore*, *Fenrir*, or *Aoede*.
- **Wake Word**: Enable local hands-free wake word activation.
- **Audio Devices**: Select dedicated microphone and output devices.

---

## 🛡️ License

This project is licensed under the MIT License.
