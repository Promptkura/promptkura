<p align="center">
  <a href="https://promptkura.me"><img src="https://promptkura.me/apple-icon" width="88" height="88" alt="Promptkura"></a>
</p>

<h1 align="center">Promptkura</h1>

<p align="center">
  The AI prompt and skill library: 13,000+ prompts, Claude skills, agents, commands and rules,<br>
  searchable and installed into your project in one command.
</p>

<p align="center">
  <a href="https://promptkura.me">Website</a> ·
  <a href="https://www.npmjs.com/package/promptkura">npm</a> ·
  <a href="https://x.com/promptkura">X</a> ·
  <a href="mailto:hello@promptkura.me">hello@promptkura.me</a>
</p>

---

## What it is

Promptkura collects the best prompts and agent skills from across the community, plus in-house **Originals**, into one library you can search by task and install straight into your AI tools.

- **13,000+ items**: prompts, Claude skills, agents, slash commands, rules and hooks
- **Works with** Claude Code, Claude.ai, Cursor, Codex, GitHub Copilot, ChatGPT, Gemini and Windsurf
- **Credit kept**: every item links back to its author and license
- **One payment, lifetime access**: see [promptkura.me](https://promptkura.me/#pricing)

## Install from the terminal

```bash
npx promptkura login                              # sign in from the browser
npx promptkura search "test driven"               # search the library
npx promptkura add obra/test-driven-development   # install into this project
```

`add` writes the item where your tool expects it (for example `.claude/skills/` for Claude Code). Pick another tool with `--tool cursor|codex|copilot`, or install for every project with `--global`.

| Command | What it does |
|---|---|
| `promptkura login` | Sign in from the browser (creates a key for this device) |
| `promptkura whoami` | Show the signed-in account |
| `promptkura search <words>` | Search the library (`--type skill`, `--tool cursor`, `-n 15`, `--json`) |
| `promptkura show <author/name>` | Print an item (`--raw`, `--json`) |
| `promptkura add <author/name>` | Install into this project (`--tool`, `--global`, `--force`, `--dry-run`) |
| `promptkura mcp install` | Connect Claude Code (or any MCP client) to Promptkura |
| `promptkura logout` | Revoke this device's key |

Requires Node.js 20 or newer.

## Use it from your AI tool (MCP)

Let Claude Code search and install items for you:

```bash
npx promptkura mcp install
```

Or add the server to any MCP client by hand:

```json
{
  "mcpServers": {
    "promptkura": {
      "type": "http",
      "url": "https://promptkura.me/mcp",
      "headers": { "Authorization": "Bearer <your key from promptkura.me/settings>" }
    }
  }
}
```

## Support

Questions, billing or a takedown request: **hello@promptkura.me**
