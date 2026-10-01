# Bitpanda Fusion plugin for Grok Build

Connect Grok Build to your [Bitpanda Fusion](https://docs.fusion.bitpanda.com) account
through the hosted Fusion MCP server. Query order books, candles, and tickers, check
balances and fee tiers, list orders and trades, and place or cancel limit and market orders.

Docs: <https://docs.fusion.bitpanda.com/getting-started-370710m0>
Tools: <https://docs.fusion.bitpanda.com/available-tools-370711m0>

## Setup

1. Create a Fusion API key in your Bitpanda account under
   **Account settings → API Keys → Fusion** (see
   [API key generation](https://docs.fusion.bitpanda.com/api-key-generation-363384m0)).
   - **Read** — market data, balances, account info, trade history
   - **Trade** — placing and cancelling orders. Only enable it if you want Grok to trade.
2. Export it before starting Grok Build:
   ```bash
   export BITPANDA_FUSION_API_KEY="<your fusion api key>"
   ```
3. In Grok Build, open `/plugin`, search for **Bitpanda Fusion**, and install.

Do not paste your API key into chat.

## Authentication

The plugin connects only to `https://mcp.fusion.bitpanda.com` (streamable HTTP).
Requests carry the API key from the `BITPANDA_FUSION_API_KEY` environment variable in
the `x-api-key` header. No credentials are stored in the plugin. Which tools are
available depends on the key's scopes.

Network endpoints:

- `https://mcp.fusion.bitpanda.com` — hosted MCP

## License

Proprietary. Use of the hosted MCP is governed by Bitpanda's terms.
