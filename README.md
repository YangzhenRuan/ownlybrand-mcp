# OwnlyBrand MCP server

[![OwnlyBrand MCP connector](https://glama.ai/mcp/connectors/com.ownlybrand/site/badges/score.svg)](https://glama.ai/mcp/connectors/com.ownlybrand/site)

**Answers whether IndiaMART, Alibaba, ThomasNet or GlobalSpec are worth paying for versus an owned website, for manufacturers and OEM parts suppliers.**

A free, public [MCP](https://modelcontextprotocol.io) server from [OwnlyBrand](https://ownlybrand.com?utm_source=github&utm_medium=readme&utm_campaign=mcp): **OwnlyBrand B2B Marketplace & Direct Sales Database**. Connect it to ChatGPT, Claude or another AI assistant and it answers from OwnlyBrand's published guides and articles, citing the page each answer comes from.

```
https://ownlybrand.com/mcp
```

No sign-in, no API key, nothing to install. Listed in the [official MCP Registry](https://registry.modelcontextprotocol.io/v0.1/servers?search=com.ownlybrand%2Fsite) as `com.ownlybrand/site`.

## What you can ask

- "We pay about ₹45,000 a year for an IndiaMART plan and got 120 BuyLeads, of which 6 turned into orders. Is it worth renewing, and what should I audit before I do?"
- "Is Alibaba Trade Assurance or Made-in-China Gold Supplier worth paying for if we make OEM auto parts and mostly want US buyers?"
- "ThomasNet costs us $12,000 a year and brought in 40 inquiries. What's our cost per lead, and how does that compare to building our own website with SEO?"
- "How fast do I need to reply to an RFQ on a B2B marketplace before the buyer moves on, and what actually improves inquiry-to-order conversion?"
- "What wholesale pricing format should a small factory publish, such as tiered MOQ pricing or quote-only, without giving away our margin?"
- "Our factory is in India with a 10-hour time difference from US buyers. How do we handle language and response times so we don't lose deals?"

## Tools

| Tool | What it does |
|---|---|
| `about_site` | Start here: what B2B marketplace costs and owned direct sales channels for manufacturers database covers (IndiaMART plan costs, BuyLeads and renewal audits, Alibaba Trade Assurance and Made-in-China Gold Supplier, ThomasNet and GlobalSpec cost per lead and ROI, Marketplace fees versus an owned website and SEO, RFQ response time and buyer inquiry conversion, Wholesale pricing formats and margin protection, Generative engine optimization for B2B manufacturers, Selling to US buyers across language and time zones), who it is for (Small to mid-sized manufacturers, OEM parts suppliers and factory owners comparing B2B marketplaces with owned channels), and its free calculators. |
| `search_site` | Search B2B marketplace costs and owned direct sales channels for manufacturers library: IndiaMART plan costs, BuyLeads and renewal audits, Alibaba Trade Assurance and Made-in-China Gold Supplier, ThomasNet and GlobalSpec cost per lead and ROI, Marketplace fees versus an owned website and SEO, RFQ response time and buyer inquiry conversion, Wholesale pricing formats and margin protection, Generative engine optimization for B2B manufacturers, Selling to US buyers across language and time zones. |
| `read_page` | The full text of one OwnlyBrand page: an article, guide, FAQ page or calculator page. |
| `ask_expert` | A question still open? With your OK, your name and email, the assistant sends it to OwnlyBrand's specialists, and a person replies by email. |

Every tool only reads OwnlyBrand's published pages, except `ask_expert`, which sends only what you approve.

## Connect it

**Claude** (claude.ai and desktop, every plan; Free allows one custom connector): Customize > Connectors > **+ Add** > **Add custom connector**. Name it, paste `https://ownlybrand.com/mcp`, choose **No sign in**, then **Add**. In a chat: **+** > Connectors, switch it on. ([Claude help](https://support.claude.com/en/articles/11175166-get-started-with-custom-connectors-using-remote-mcp))

**ChatGPT** (Pro, Business, Enterprise, Edu; web): **Plugins** > **+** > **Add custom MCP server**. Name it, paste the URL under Connection, accept the notice, **Create as a plugin**. In a new chat type **@** and pick it. ([OpenAI help](https://help.openai.com/en/articles/12584461))

**Claude Code**:
```bash
claude mcp add --transport http ownlybrand https://ownlybrand.com/mcp
```
Or clone this repo: its `.mcp.json` connects it for the project.

**Cursor** (`~/.cursor/mcp.json`):
```json
{ "mcpServers": { "ownlybrand": { "url": "https://ownlybrand.com/mcp" } } }
```

**VS Code (GitHub Copilot)**: Command Palette > **MCP: Add Server** > HTTP > paste the URL.

**Gemini CLI**:
```bash
gemini mcp add --transport http ownlybrand https://ownlybrand.com/mcp
```

## Try it without an AI

```bash
curl -s https://ownlybrand.com/mcp -H 'content-type: application/json' \
  -d '{"jsonrpc":"2.0","id":1,"method":"tools/call","params":{"name":"search_site","arguments":{"query":"IndiaMART renewal audit"}}}'
```

## More from OwnlyBrand

- Website: [ownlybrand.com](https://ownlybrand.com?utm_source=github&utm_medium=readme&utm_campaign=mcp)
- Questions: [ownlybrand.com/contact](https://ownlybrand.com/contact?utm_source=github&utm_medium=readme&utm_campaign=mcp)

Answers are general information from OwnlyBrand's published pages.

## License

This repository (README and config) is MIT licensed. The server is operated by OwnlyBrand.
