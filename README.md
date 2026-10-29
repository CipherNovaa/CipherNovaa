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

<!-- MORE PROJECTS: filled from the inventory -->

## How I build with agents

codec is the clearest example: over 110,000 lines of C++, QML and Python, built in four months with Claude Code. What that looks like in practice:

- **A memory the agents work from.** A project map (`CLAUDE.md`) and 89 topic notes record every subsystem, decision and trap, so each session starts where the last one stopped instead of re-learning the codebase.
- **The right agent for the job.** Parallel read-only explorers map a 20,000-line server before I change it; a dedicated forensics agent works through cast telemetry on the hardest Dolby Vision bugs; the main session drives the build.
- **Audits as workflows.** A repeatable multi-agent audit (a finder model per slice of the codebase, a skeptical checker model re-verifying each finding) ran twice over codec: 146 and 104 findings, fixed and verified.
- **Custom skills** that encode how a subsystem is reviewed, or how an overnight media pipeline is checked, so the method is reusable rather than remembered.
- **Proof over telemetry.** An offscreen screenshot harness for every view, a headless preview of the TV receiver, frame meters, and captures from the actual television. An agent's "it works" isn't done until the picture says so.
- **Writing the hard parts down.** [codec's engineering notes](https://github.com/CipherNovaa/codec/blob/main/docs/ENGINEERING.md) tell nine of the hardest bugs: what was seen, what it really was, and how it was proven.

## Toolbox

`C++` `C` `Python` `QML / Qt 6` `JavaScript` `Bash` · `FFmpeg` `libmpv` `NVENC` `Vulkan` `libplacebo` · `Google Cast` `DASH / HLS` `Dolby Vision` · `PipeWire` `D-Bus` `systemd` `Hyprland` · `Claude Code` (subagents, skills, workflows, MCP)
