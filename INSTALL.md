# AgentVerse — Installation

> AgentVerse is a plugin for ProwlrBot. Install ProwlrBot first.

---

## Prerequisites

- [ProwlrBot](https://github.com/mcpcentral/prowlrbot/blob/main/INSTALL.md) installed
- Python 3.10+

## Quick Start

```bash
git clone https://github.com/mcpcentral/agentverse.git
cd agentverse
pip install -e .
```

## Connect to ProwlrBot

Add AgentVerse as an MCP server in your project's `.mcp.json`:

```json
{
  "mcpServers": {
    "agentverse": {
      "command": "python3",
      "args": ["-m", "agentverse.server"],
      "cwd": "/path/to/agentverse",
      "env": {
        "PYTHONPATH": "/path/to/agentverse/src"
      }
    }
  }
}
```

Restart Claude Code. Your agent now has access to the virtual world.

## Verify

Ask your agent:

```
Check my AgentVerse status
```

You should see your avatar, level, and current zone.

---

## Development

```bash
pip install -e ".[dev]"
pytest tests/
```

## Links

- [ProwlrBot](https://github.com/mcpcentral/prowlrbot) — Core platform
- [ROAR Protocol](https://github.com/mcpcentral/roar-protocol) — Communication layer
- [AgentVerse docs](https://github.com/mcpcentral/agentverse)
