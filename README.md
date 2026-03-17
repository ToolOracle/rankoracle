# RankOracle — SEO Intelligence MCP Server

**The first standalone SEO MCP server.** 13 AI-native tools for keyword research, SERP analysis, domain audits, competitor gaps, and on-page optimization — delivered via MCP.

> Built by [ToolOracle](https://tooloracle.io) | Powered by DataForSEO

## Connect in 30 seconds

```bash
npx -y mcp-remote https://mcp.tooloracle.io/mcp/
```

### Claude Desktop
```json
{
  "mcpServers": {
    "rankoracle": {
      "command": "npx",
      "args": ["-y", "mcp-remote", "https://mcp.tooloracle.io/mcp/"]
    }
  }
}
```

## 13 Tools (12 live + 1 demo)

| Tool | Credits | Description |
|------|---------|-------------|
| `keyword_research` | 10 | Volume, CPC, competition, monthly trends |
| `domain_overview` | 3 | Organic keywords, traffic estimate, position distribution |
| `competitor_gap` | 3 | Keywords your competitor ranks for but you don't |
| `check_ranking` | 1 | Where a domain ranks for a keyword (top 100) |
| `serp_snapshot` | 1 | Top 10 Google results with SERP features |
| `content_score` | 1 | On-page SEO score, readability, recommendations |
| `heading_analysis` | 1 | H1-H4 structure analysis with issues |
| `title_optimizer` | 1 | Title tag analysis + optimized suggestions |
| `meta_generator` | 1 | Meta title + description audit and generation |
| `rank_tracker` | 1/kw | Track positions for multiple keywords at once |
| `serp_alert` | 1 | Position change tracking over time |
| `backlink_check` | 1 | Backlink summary (demo — needs Backlinks subscription) |
| `health_check` | 0 | Server status, pricing, tool info |

## Pricing

Credit-based. Each tool costs a fixed number of credits per call.

| Tier | Price | Credits/Month | Per Credit |
|------|-------|---------------|------------|
| Free | $0 | 50 | — |
| Starter | $49/mo | 500 | $0.098 |
| Pro | $149/mo | 2,000 | $0.075 |
| Agency | $349/mo | 6,000 | $0.058 |

### Credit Top-Up Packs (instant, no commitment)

| Pack | Credits | Price | Per Credit |
|------|---------|-------|------------|
| 100 | 100 | $20 | $0.20 |
| 250 | 250 | $39 | $0.156 |
| 500 | 500 | $69 | $0.138 |
| 1,000 | 1,000 | $119 | $0.119 |

## Example: Keyword Research

```bash
curl -X POST https://mcp.tooloracle.io/mcp/ \
  -H "Content-Type: application/json" \
  -d '{
    "jsonrpc": "2.0",
    "id": 1,
    "method": "tools/call",
    "params": {
      "name": "keyword_research",
      "arguments": {"keyword": "SEO tools", "country": "US"}
    }
  }'
```

Response:
```json
{
  "keyword": "seo tools",
  "country": "US",
  "volume": 18100,
  "cpc": 8.5,
  "competition": 0.87,
  "competition_level": "HIGH",
  "monthly_searches": [...],
  "_mode": "live"
}
```

## Why RankOracle?

- **First mover**: No other standalone SEO MCP exists
- **Real data**: Powered by DataForSEO (live Google SERP, not cached)
- **AI-native**: Built for Claude, Cursor, Windsurf — not a dashboard wrapper
- **Fair pricing**: Ahrefs API starts at $449/mo. RankOracle Agency is $349/mo with 6,000 credits.

## Endpoints

| URL | Purpose |
|-----|---------|
| `https://mcp.tooloracle.io/mcp/` | MCP StreamableHTTP endpoint |
| `https://mcp.tooloracle.io/health` | Health check + tool list |
| `https://tooloracle.io` | Landing page |
| `https://tooloracle.io/llms.txt` | LLM discovery |

## Status

- **Version**: 1.2.0
- **Tools**: 13 (12 live, 1 demo)
- **Uptime**: monitored 24/7

## License

Proprietary. The MCP server is hosted and operated by ToolOracle. This repository contains documentation and configuration files.

---

**[tooloracle.io](https://tooloracle.io)** — AI-native tools, MCP-delivered.
