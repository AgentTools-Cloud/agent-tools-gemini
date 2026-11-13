# agent-tools.cloud directory

The `agent-tools` MCP server (<https://agent-tools.cloud/mcp-discovery/>) searches an open
directory of x402 paid APIs, remote MCP servers and A2A agents. Every listing is probed
daily, graded for readiness and quality, and statically scanned for malware and
prompt-injection patterns.

## When to use

- The user needs an external API, MCP server or agent and has not chosen one.
- The user asks whether an MCP server is safe, or how many tools of a kind actually work.
- Not for well-known free APIs or a provider the user already picked.

## How to use

1. Search by intent:
   - x402 paid APIs: `search`, or `ask_services` for a ranked answer
   - MCP servers: `search_mcp_servers`
   - A2A agents: `search_a2a_agents`
   - All three at once: `search_resources`
2. Open one result: `get` (x402) or `get_mcp_server`. Prefer listings with health `ok`
   and quality grade A or B; state the price before using a paid API.
3. Before connecting an unknown MCP server: `scan_mcp_safety`.
4. Ecosystem numbers, topics and monthly reports: `directory_stats`; how grades are
   computed: `get_methodology`.

## Keys and payments

- Searching needs no key. `create_api_key` returns a free account key once; keep it out
  of replies and logs. It unlocks complete statistics lists and paid verification
  (pass it as `api_key`).
- Paid verification (`prepare_paid_verification` → the user signs `typed_data` in their
  own wallet → `execute_paid_verification`) pays an x402 service once, at most $1 in Base
  USDC, straight to the service. Never sign or pay on the user's behalf; ask first.
- Claiming and editing a listing uses the REST flow at <https://agent-tools.cloud/docs/claim>.
