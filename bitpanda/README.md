# Bitpanda plugin for Grok Build

Connect Grok Build to your [Bitpanda](https://www.bitpanda.com) account through the
hosted Bitpanda MCP server. Check your portfolio and its performance, browse assets
and tickers, request and accept trading quotes, and stake or unstake with Bitpanda Earn.

Docs: <https://docs.public.bitpanda.com/getting-started-589286f0>

## Setup

1. Create an API key in your Bitpanda account (see
   [API key generation](https://docs.public.bitpanda.com/api-key-generation)).
   Only grant the scopes you need — omit trading/staking scopes for read-only use.
2. Export it before starting Grok Build:
   ```bash
   export BITPANDA_API_KEY="<your api key>"
   ```
3. In Grok Build, open `/plugin`, search for **Bitpanda**, and install.

Do not paste your API key into chat.

## Authentication

The plugin connects only to `https://mcp.public.bitpanda.com` (streamable HTTP).
Requests carry the API key from the `BITPANDA_API_KEY` environment variable in the
`x-api-key` header. No credentials are stored in the plugin.

Network endpoints:

- `https://mcp.public.bitpanda.com` — hosted MCP

Rate limits are applied per API key; see
[API and MCP Rate Limits](https://docs.public.bitpanda.com/api-and-mcp-rate-limits).

## License

Proprietary. Use of the hosted MCP is governed by Bitpanda's terms.
