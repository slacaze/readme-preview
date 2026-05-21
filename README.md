# MathWorks Agentic Installer

[![Release](https://img.shields.io/github/v/release/mathworks/agentic-installer?style=flat-square)](https://github.com/mathworks/agentic-installer/releases)

Install and manage MathWorks agentic toolkits with a single command. Handles MATLAB Agentic Toolkit, Simulink Agentic Toolkit, and MCP servers — with agent auto-detection, version management, and built-in updates.

## ⚡ Quick Start

<details open>
<summary><strong>Linux (bash)</strong></summary>

```bash
curl -fsSL https://github.com/mathworks/agentic-installer/releases/latest/download/agentic-installer-linux-amd64 -o agentic-installer \
  && chmod +x agentic-installer \
  && ./agentic-installer install
```

</details>

<details>
<summary><strong>macOS (zsh)</strong></summary>

```bash
curl -fsSL https://github.com/mathworks/agentic-installer/releases/latest/download/agentic-installer-darwin-arm64 -o agentic-installer \
  && chmod +x agentic-installer \
  && ./agentic-installer install
```

</details>

<details>
<summary><strong>Windows (PowerShell)</strong></summary>

```powershell
Invoke-WebRequest -Uri "https://github.com/mathworks/agentic-installer/releases/latest/download/agentic-installer-windows-amd64.exe" -OutFile "agentic-installer.exe"; .\agentic-installer.exe install
```

</details>

---

The installer auto-detects your coding agents (Claude Code, GitHub Copilot, Codex, Amp, Gemini CLI) and configures the appropriate toolkits for each. It also sets up all specified installed MATLAB releases.

## Installing from MATLAB Directly

If you prefer to install from within MATLAB, you have two options:

**Option A — File Exchange**

1. Download the toolbox (`.mltbx`) from [MathWorks Agentic Installer on File Exchange](https://www.mathworks.com/matlabcentral/fileexchange/TODO)
2. Open the `.mltbx` file in MATLAB and follow the installation steps
3. Run `install_agentic_toolkits` in the MATLAB Command Window

**Option B — Add-On Manager**

1. Open the **Add-On Manager** in MATLAB (Home tab → Add-Ons → Get Add-Ons)
2. Search for `MathWorks Agentic Installer`, `MATLAB Agentic Toolkit`, or `Simulink Agentic Toolkit`
3. Install the Add-On
4. Run `install_agentic_toolkits` in the MATLAB Command Window

## What Gets Installed

| Component | Description |
|-----------|-------------|
| **MATLAB Agentic Toolkit** | Skills, rules, and context for MATLAB workflows |
| **Simulink Agentic Toolkit** | Model-based design guidance for agents |
| **MATLAB MCP Server** | Tool-use bridge between agents and MATLAB |

## Commands

```bash
agentic-installer install      # Install/update all toolkits
agentic-installer configure    # Re-run agent detection and configuration
agentic-installer status       # Show what's installed and configured
agentic-installer uninstall    # Remove all installed components
```

## Options

```bash
agentic-installer install --agent claude      # Configure for a specific agent only
agentic-installer install --proxy config.yaml # Use a custom proxy configuration
... blah blah blah ...
```
