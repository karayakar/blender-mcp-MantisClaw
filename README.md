<<<<<<< copilot/create-readme-for-mantisclaw
<p align="center">
  <img src="https://github.com/karayakar/MantisClaw-v1/blob/main/mantis-claw-logo.png" width="400"/>
</p>

<h1 align="center">blender-mcp-MantisClaw</h1>

<p align="center">
  <strong>Control Blender directly from MantisClaw</strong><br/>
  Use WhatsApp, Telegram, or Slack to command Blender with AI through the MantisClaw agent platform.
</p>

<p align="center">
  <a href="https://mantisclaw.yapzek.ai" target="_blank">🦗 Download MantisClaw</a> &nbsp;•&nbsp;
  <a href="https://mantisclaw.yapzek.ai" target="_blank">📖 MantisClaw Docs</a>
</p>

---

## 🦗 What is blender-mcp-MantisClaw?

**blender-mcp-MantisClaw** is a [MantisClaw](https://mantisclaw.yapzek.ai) skill that connects [MantisClaw](https://mantisclaw.yapzek.ai)'s autonomous agent platform to [Blender](https://www.blender.org/) via the **Model Context Protocol (MCP)**.

It lets you control Blender directly from **WhatsApp, Telegram, or Slack** by issuing natural language commands to your MantisClaw agent — no need to open Blender's UI.

```
WhatsApp / Telegram / Slack
         │
         ▼
   MantisClaw Agent
         │
         ▼
  blender-mcp skill
         │
         ▼
  Blender MCP Server
         │
         ▼
      Blender
```

---

## ✨ Features

- **Chat-driven Blender control** — Send commands from WhatsApp, Telegram, or Slack and have MantisClaw execute them in Blender in real time.
- **Natural language 3D modeling** — Create, modify, and delete meshes and objects using plain English prompts.
- **Python script execution** — Run arbitrary Blender Python (`bpy`) scripts directly from chat.
- **Scene inspection** — Query scene state, object properties, and capture Blender viewport screenshots.
- **Material & texture control** — Apply and change materials, colors, and textures via chat commands.
- **Asset integration** — Search and import assets from Poly Haven, Sketchfab, and AI model generators.
- **Autonomous workflow automation** — Let MantisClaw autonomously plan and execute multi-step 3D tasks.
- **Scheduled rendering** — Schedule rendering jobs and receive output files directly in chat.
- **Secure execution** — All operations run locally; API keys and credentials are injected at runtime and never exposed to the LLM.

---

## 📋 Requirements

| Requirement | Version |
|---|---|
| [MantisClaw](https://mantisclaw.yapzek.ai) | Latest (Windows) |
| [Blender](https://www.blender.org/download/) | 3.0 or later |
| Python | 3.10 or later |
| Operating System | Windows |

---

## 🚀 Setup

### 1. Download MantisClaw

Download and install MantisClaw from [mantisclaw.yapzek.ai](https://mantisclaw.yapzek.ai).

Follow the MantisClaw setup wizard to:
- Connect your WhatsApp, Telegram, or Slack account.
- Configure your LLM provider (API key).
- Launch the MantisClaw agent.

### 2. Install the Blender Addon

1. Download `blender_mcp_addon.py` from the [`/addon`](./addon) directory of this repository (or the [latest release](../../releases/latest)).
2. Open Blender and go to **Edit → Preferences → Add-ons → Install**.
3. Select the downloaded file and enable the addon (tick the checkbox).
4. In Blender's **N panel** (press `N` in the viewport), find the **MCP** tab.
5. Click **Start MCP Server** to begin listening for connections.

### 3. Add the Skill to MantisClaw

1. Open MantisClaw and navigate to **Skills**.
2. Click **Import Skill** and select the `blender_mcp_skill.json` file from the [`/skill`](./skill) directory of this repository.
3. Configure the skill with the Blender MCP server address (default: `localhost:9876`).
4. Save and activate the skill.

### 4. Connect & Start Controlling Blender

Your MantisClaw agent can now control Blender. Send a command from your connected chat app:

```
create a red cube in the center of the scene
```

MantisClaw will interpret the request, execute the appropriate Blender operations, and confirm the result back in chat.

---

## 💬 Example Commands

Once configured, you can send natural language commands from any connected chat platform:

```
# Object creation
create a sphere with radius 2

# Object modification
scale the selected object to 1.5x on the X axis

# Materials
apply a blue metallic material to the cube

# Scene inspection
take a screenshot of the current viewport

# Python scripting
run this bpy script: bpy.ops.mesh.primitive_torus_add()

# Rendering
render the current scene and send me the image

# Asset import
import a wooden floor texture from Poly Haven
```

---

## 🔄 How It Works

1. **User sends a message** via WhatsApp, Telegram, or Slack.
2. **MantisClaw Router** maps the message to the `blender-mcp` skill.
3. **The Blender MCP skill** translates the request into MCP tool calls.
4. **Blender MCP Server** (running inside Blender) receives and executes the commands using Blender's Python API (`bpy`).
5. **Result** (confirmation, screenshot, rendered image, etc.) is returned to the chat.

---

## 🔐 Security

- All operations run **locally** on your machine.
- API keys and credentials are **injected at runtime** by MantisClaw and never sent to the LLM.
- The Blender MCP server listens only on `localhost` by default — it is not exposed to the internet.
- Follows MantisClaw's **local-first architecture** principles.

---

## 🛠 Troubleshooting

| Problem | Solution |
|---|---|
| Blender addon not connecting | Ensure the MCP server is started from the N panel in Blender. |
| Commands not recognized | Check that the `blender-mcp` skill is active in MantisClaw. |
| Wrong Blender version | Blender 3.0 or later is required. |
| Connection refused error | Verify the host/port in the skill config matches what Blender shows. |

---

## 🌍 About MantisClaw

[MantisClaw](https://mantisclaw.yapzek.ai) is a Windows-based autonomous agent platform by [Yapzek.ai](https://yapzek.ai) that turns everyday messaging apps into **operational control interfaces for AI agents**.

Instead of dashboards and complex control panels, MantisClaw lets teams run real operations directly from **WhatsApp, Telegram, and Slack** through a powerful skill and tool execution engine backed by local-first, secure data storage.

[⬇ Download MantisClaw](https://mantisclaw.yapzek.ai)

---

## 🧑‍💻 Maintained by

**Karay Akar** — [github.com/karayakar](https://github.com/karayakar)

---

## 📜 License

License details coming soon.
=======
# blender-mcp-MantisClaw
Control Blender directly from MantisClaw  https://mantisclaw.yapzek.ai


This code modified for Mantis
Reference
https://github.com/ahujasid/blender-mcp/blob/main/addon.py
>>>>>>> main
