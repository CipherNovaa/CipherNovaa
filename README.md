```
 ██████╗██╗██████╗ ██╗  ██╗███████╗██████╗ ███╗   ██╗ ██████╗ ██╗   ██╗ █████╗  █████╗
██╔════╝██║██╔══██╗██║  ██║██╔════╝██╔══██╗████╗  ██║██╔═══██╗██║   ██║██╔══██╗██╔══██╗
██║     ██║██████╔╝███████║█████╗  ██████╔╝██╔██╗ ██║██║   ██║██║   ██║███████║███████║
██║     ██║██╔═══╝ ██╔══██║██╔══╝  ██╔══██╗██║╚██╗██║██║   ██║╚██╗ ██╔╝██╔══██║██╔══██║
╚██████╗██║██║     ██║  ██║███████╗██║  ██║██║ ╚████║╚██████╔╝ ╚████╔╝ ██║  ██║██║  ██║
 ╚═════╝╚═╝╚═╝     ╚═╝  ╚═╝╚══════╝╚═╝  ╚═╝╚═╝  ╚═══╝ ╚═════╝   ╚═══╝  ╚═╝  ╚═╝╚═╝  ╚═╝
```

```
┌─ CODEC ──────────────────────────────────────────────────────────── 140.85 ─┐
│  ROLE      independent software developer · building with AI agents         │
│  METHOD    I design the system, direct AI agents to build it, and prove     │
│            every change on the real hardware                                │
│  STACK     C++ / Qt 6 · QML · Python · C · FFmpeg · Linux                   │
│  NOW       codec v1.49  ·  twine-pc                                         │
└─────────────────────────────────────────────────────────────────────────────┘
```

I build ambitious software with AI agents as my team: a media player that casts true 4K Dolby Vision through its own Cast receiver, a PlayStation shooter decompiled to byte-identical C and ported to PC. I set the architecture and the bar, split the work across agents, and verify the result on real screens, real TVs and real networks.

## Featured

<table>
<tr>
<td width="50%" valign="top">

### [codec](https://github.com/CipherNovaa/codec)
A private cinema for your own films. Qt 6 / QML on libmpv, a Python hub, and its own Google Cast receiver: **Dolby Vision copied to the TV, never re-encoded**, synced watch parties from one link, YouTube with or without an account, all drawn in hand-made pixel chrome.

`C++ 20` `QML` `Python` `FFmpeg` `Cast` · 976 commits · 66 releases

</td>
<td width="50%" valign="top">

### [twine-pc](https://github.com/CipherNovaa/twine-pc)
A native PC port of *007: The World Is Not Enough* (PS1). All **14 executables decompiled to byte-identical C**, then given a new engine room: Vulkan and software renderers, smooth motion at any refresh rate, modern controls, and an all-new Endless Mode.

`C` `Vulkan` `Windows` `Linux` · decompilation

</td>
</tr>
</table>

### Agents

| | |
|---|---|
| **[agent-skills](https://github.com/CipherNovaa/agent-skills)** | A two-agent system: Claude as architect, a local model as operator. A skill contract with earned autonomy and mandatory verification, escalation from the local model to Claude, a drift-detecting janitor, and one memory shared by both |
| **[supernote-agent](https://github.com/CipherNovaa/supernote-agent)** | Handwritten notes on an e-ink tablet become clean Obsidian notes through local LLMs. Handwritten `//commands` trigger actions, and plain-English feedback turns into JSON actions that teach it your style |

### Reverse engineering

| | |
|---|---|
| **[codecos-remote](https://github.com/CipherNovaa/codecos-remote)** | A universal remote's BLE protocol and two-chip firmware, reversed and rebuilt as custom firmware with an e-paper screensaver, then wrapped in a desktop control app. Handed between Claude, Codex and Fable along the way |
| **[ac6-crt-5to4](https://github.com/CipherNovaa/ac6-crt-5to4)** | Armored Core VI on a 5:4 CRT: a D3D12 hook for the 3D, and Scaleform tools to re-lay the HUD and menus, with a capture tool so the agent could see every change |
| **[mgs4-crt](https://github.com/CipherNovaa/mgs4-crt)** | Metal Gear Solid 4 filling a 5:4 CRT: replaces the letterbox blit and re-fits every 2D sprite to its true shape from its vertices and shader constants |

### Tools

| | |
|---|---|
| **[hyprule](https://github.com/CipherNovaa/hyprule)** | A GTK4 window-rule manager for Hyprland's Lua config |
| **[pipewire-surround](https://github.com/CipherNovaa/pipewire-surround)** | Binaural 7.1 for headphones on PipeWire, generated from HRTF data, switching automatically with your output |
| **[keybr-ws](https://github.com/CipherNovaa/keybr-ws)** | A live typing dashboard for keybr.com: browser extension → native host → ImGui |
| **[dotfiles](https://github.com/CipherNovaa/dotfiles)** | A Hyprland desktop where one wallpaper rethemes about fifteen apps, with Quickshell widgets and a CRT gaming corner |

## How I build with agents

codec is the clearest example: over 110,000 lines of C++, QML and Python, built in four months with Claude Code. What that looks like in practice:

- **A memory the agents work from.** A project map (`CLAUDE.md`) and 89 topic notes record every subsystem, decision and trap, so each session starts where the last one stopped instead of re-learning the codebase.
- **The right agent for the job.** Parallel read-only explorers map a 20,000-line server before I change it; a dedicated forensics agent works through cast telemetry on the hardest Dolby Vision bugs; the main session drives the build.
- **Audits as workflows.** A repeatable multi-agent audit (a finder model per slice of the codebase, a skeptical checker model re-verifying each finding) ran twice over codec: 146 and 104 findings, fixed and verified.
- **Custom skills** that encode how a subsystem is reviewed, or how an overnight media pipeline is checked, so the method is reusable rather than remembered. [agent-skills](https://github.com/CipherNovaa/agent-skills) is the same idea grown into a framework: a skill contract with earned autonomy, run by a local model and escalated to Claude.
- **Giving agents eyes.** Tools that capture what's really on screen (a game's backbuffer, a TV's output, every app view offscreen) so an agent checks its change against the real picture.
- **Proof over telemetry.** An offscreen screenshot harness for every view, a headless preview of the TV receiver, frame meters, and captures from the actual television. An agent's "it works" isn't done until the picture says so.
- **Writing the hard parts down.** [codec's engineering notes](https://github.com/CipherNovaa/codec/blob/main/docs/ENGINEERING.md) tell nine of the hardest bugs: what was seen, what it really was, and how it was proven.

## Toolbox

`C++` `C` `Python` `QML / Qt 6` `JavaScript` `Bash` · `FFmpeg` `libmpv` `NVENC` `Vulkan` `libplacebo` · `Google Cast` `DASH / HLS` `Dolby Vision` · `PipeWire` `D-Bus` `systemd` `Hyprland` · `Claude Code` (subagents, skills, workflows, MCP)
