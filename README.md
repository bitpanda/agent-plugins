# Bitpanda agent plugins

Official Bitpanda plugins for AI coding agents. Each plugin connects your agent to one of Bitpanda's hosted MCP (Model Context Protocol) servers.

| Plugin | What it does | MCP server | Docs |
|---|---|---|---|
| [`bitpanda`](./bitpanda) | Portfolio and performance, assets and tickers, trading quotes, and Bitpanda Earn (staking) | `https://mcp.public.bitpanda.com` | [docs.public.bitpanda.com](https://docs.public.bitpanda.com) |
| [`bitpanda-fusion`](./bitpanda-fusion) | Order books, candles and tickers, balances and fee tiers, and order management on Bitpanda Fusion | `https://mcp.fusion.bitpanda.com` | [docs.fusion.bitpanda.com](https://docs.fusion.bitpanda.com) |

Both plugins authenticate with a Bitpanda API key that you set as an environment variable. The key is sent as the `x-api-key` header, and no credentials are stored in this repo. Each plugin's README covers setup and the scopes it needs.

These plugins contain only MCP server configuration: no skills, hooks, scripts or executable code.

## License

Proprietary. Use of Bitpanda's hosted MCP servers is governed by Bitpanda's terms.
