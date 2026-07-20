# ScrapingAnt: Native API Reference

A consolidated summary of ScrapingAnt's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://docs.scrapingant.com/
- **OpenAPI specification:** https://api.scrapingant.com/openapi.json
- **API base URL:** `https://api.scrapingant.com/v2`

## Authentication

### API Key

Authenticate ScrapingAnt requests with an API key provided as the x-api-key query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.scrapingant.com/request-response-format)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `409,423,500`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Extract Markdown From URL](actions/extract-markdown-from-url.md) | `GET /markdown` | [docs](https://docs.scrapingant.com/llm-markdown) |
| [Extract Structured Data From URL](actions/extract-structured-data-from-url.md) | `GET /extract` | [docs](https://docs.scrapingant.com/ai-data-extraction/ai-extractor) |
| [Get API Credits Usage](actions/get-api-credits-usage.md) | `GET /usage` | [docs](https://docs.scrapingant.com/api-credits-usage) |
| [Scrape URL](actions/scrape-url.md) | `GET /general` | [docs](https://docs.scrapingant.com/request-response-format) |
| [Scrape URL With DELETE](actions/scrape-url-with-delete.md) | `DELETE /general` | [docs](https://docs.scrapingant.com/post-put-delete) |
| [Scrape URL With Extended JSON](actions/scrape-url-with-extended-json.md) | `GET /extended` | [docs](https://docs.scrapingant.com/json-response) |
| [Scrape URL With PATCH](actions/scrape-url-with-patch.md) | `PATCH /general` | [docs](https://docs.scrapingant.com/post-put-delete) |
| [Scrape URL With POST](actions/scrape-url-with-post.md) | `POST /general` | [docs](https://docs.scrapingant.com/post-put-delete) |
| [Scrape URL With PUT](actions/scrape-url-with-put.md) | `PUT /general` | [docs](https://docs.scrapingant.com/post-put-delete) |
