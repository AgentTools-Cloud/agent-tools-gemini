# Agent Tools — Gemini CLI extension

Find **x402 paid APIs**, **MCP servers** and **A2A agents** by intent from Gemini CLI,
backed by the open directory at [agent-tools.cloud](https://agent-tools.cloud).

```bash
gemini extensions install https://github.com/AgentTools-Cloud/agent-tools-gemini
```

The extension connects Gemini CLI to the hosted MCP server
`https://agent-tools.cloud/mcp-discovery/` (Streamable HTTP, no API key, 23 tools) and adds
a short `GEMINI.md` telling the model when and how to use it.

Example prompts:

- "Find a paid API that returns Twitter follower counts and tell me its price."
- "Which MCP servers can query Postgres? Check the top one for safety first."
- "Is there an A2A agent that can translate documents?"

The tools only discover and recommend. They never pay or sign on your behalf.

- Website: https://agent-tools.cloud
- Other installs (PyPI `agent-tools-mcp`, official MCP Registry, ClawHub skill):
  https://github.com/AgentTools-Cloud/AgentToolsCollection/tree/main/agent-tools-mcp

License: Apache-2.0
