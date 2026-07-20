# Quick Scraper: Native API Reference

A consolidated summary of Quick Scraper's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://quickscraper.co/docs/
- **API base URL:** `https://api.quickscraper.co`

## Authentication

### API Key

Use your Quick Scraper API key from the Quick Scraper dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://quickscraper.co/docs/)

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | `GET /account` | [docs](https://quickscraper.co/docs/) |
| [Parse URL](actions/parse-url.md) | `GET /parse` | [docs](https://quickscraper.co/docs/#basic-usage) |
