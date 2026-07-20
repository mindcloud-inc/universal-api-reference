# ScrapeUnblocker: Native API Reference

A consolidated summary of ScrapeUnblocker's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://www.scrapeunblocker.com/documentation
- **API base URL:** `https://scrapeunblocker.p.rapidapi.com`

## Authentication

### RapidAPI Key

Use a ScrapeUnblocker RapidAPI subscription key for authenticated requests.

### Credentials

- **API Key:** `apiKey` · required · Your RapidAPI subscription key for ScrapeUnblocker.

Send these headers with each API request:

```http
x-rapidapi-key: <apiKey>
```

[Official authentication documentation](https://www.scrapeunblocker.com/documentation)

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Page Source](actions/get-page-source.md) | `POST /getPageSource` | [docs](https://www.scrapeunblocker.com/documentation) |
