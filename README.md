# WebDataTools Domain & website intelligence MCP server
`webdatatools-domain-mcp`

An MCP server with 11 domain & website intelligence tools for AI agents — Claude Desktop, Cursor, Cline or any MCP client. WHOIS/RDAP, DNS and e-mail security (SPF, DKIM, DMARC), TLS and security headers, subdomains, tech stack, contacts, SEO, Core Web Vitals, sitemaps and Wayback page diffs for any domain.

**This server uses *your own* Apify API token.** Every tool call runs a [WebDataTools](https://apify.com/webdatatools) Actor under your Apify account and is billed to your Apify credit — pay per result, the price is in each tool description. Your token is only sent to Apify's API.

## Quick start

Requires Node.js 18+.

```bash
APIFY_TOKEN=apify_api_... npx -y github:paulet4a-commits/webdatatools-domain-mcp
```

Get a free token (the free plan includes monthly credit): https://console.apify.com/settings/integrations

## Claude Desktop / Cursor

Add this to `claude_desktop_config.json` (Claude Desktop) or `.cursor/mcp.json` (Cursor):

```json
{
  "mcpServers": {
    "webdatatools-domain": {
      "command": "npx",
      "args": [
        "-y",
        "github:paulet4a-commits/webdatatools-domain-mcp"
      ],
      "env": {
        "APIFY_TOKEN": "apify_api_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
      }
    }
  }
}
```

## Tools (11)

| Tool | What it does | Price (free plan) | Backing Actor |
|---|---|---|---|
| `contact_extractor` | Email Extractor — Website Contact & Social Finder | $0.01 / result | [Actor](https://apify.com/webdatatools/contact-extractor) |
| `tech_stack_detector` | Tech Stack Detector — Wappalyzer & BuiltWith Alternative | $0.02 / result | [Actor](https://apify.com/webdatatools/tech-stack-detector) |
| `dns_email_security_checker` | Domain DNS & Email Security Checker | $0.005 / result | [Actor](https://apify.com/webdatatools/dns-email-security-checker) |
| `domain_security_audit` | Domain Security Audit (TLS, HTTP headers, redirects, robots) | $0.005 / result | [Actor](https://apify.com/webdatatools/domain-security-audit) |
| `subdomain_finder` | Subdomain Finder (Certificate Transparency) | $0.0005 / result | [Actor](https://apify.com/webdatatools/subdomain-finder) |
| `core_web_vitals_audit` | Bulk Core Web Vitals & PageSpeed Audit | $0.005 / result | [Actor](https://apify.com/webdatatools/core-web-vitals-audit) |
| `seo_page_audit` | On-Page SEO Audit | $0.002 / result | [Actor](https://apify.com/webdatatools/seo-page-audit) |
| `sitemap_extractor` | Sitemap URL Extractor & Change Monitor | $0.0002 / result | [Actor](https://apify.com/webdatatools/sitemap-extractor) |
| `wayback_page_diff` | Wayback Machine Snapshot & Page Change Tracker | $0.003 / result | [Actor](https://apify.com/webdatatools/wayback-page-diff) |
| `domain_whois_rdap` | Bulk Domain WHOIS & RDAP Lookup | $0.003 / Domain | [Actor](https://apify.com/webdatatools/domain-whois-rdap) |
| `css_selector_extractor` | Web Scraper — CSS Selector & Data Extractor | $0.002 / Page | [Actor](https://apify.com/webdatatools/css-selector-extractor) |

## More WebDataTools MCP servers

- [webdatatools-mcp-server](https://github.com/paulet4a-commits/webdatatools-mcp-server) — the 10 most popular tools in one server
- [webdatatools-rag-mcp](https://github.com/paulet4a-commits/webdatatools-rag-mcp) — Web content for AI & RAG
- [webdatatools-social-mcp](https://github.com/paulet4a-commits/webdatatools-social-mcp) — Search, video & social data
- [webdatatools-leads-mcp](https://github.com/paulet4a-commits/webdatatools-leads-mcp) — Leads, jobs & company data
- [webdatatools-dev-mcp](https://github.com/paulet4a-commits/webdatatools-dev-mcp) — Developer, app & research data

## License

MIT
