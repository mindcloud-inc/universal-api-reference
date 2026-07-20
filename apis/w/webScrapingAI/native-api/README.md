# WebScraping.AI: Native API Reference

A consolidated summary of WebScraping.AI's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://webscraping.ai/docs
- **OpenAPI specification:** https://webscraping.ai/openapi.yml
- **API base URL:** `https://api.webscraping.ai`

## Authentication

### API Key

Authenticate requests with your WebScraping.AI API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://webscraping.ai/docs)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Ask Questions About a Page](actions/ask-questions-about-a-page.md) | `GET /ai/question` | [docs](https://webscraping.ai/docs#ai-question) |
| [Extract Structured Fields](actions/extract-structured-fields.md) | `GET /ai/fields` | [docs](https://webscraping.ai/docs#ai-fields) |
| [Get Page HTML](actions/get-page-html.md) | `GET /html` | [docs](https://webscraping.ai/docs#html) |
| [Get Page Text](actions/get-page-text.md) | `GET /text` | [docs](https://webscraping.ai/docs#text) |
| [Get Selected HTML](actions/get-selected-html.md) | `GET /selected` | [docs](https://webscraping.ai/docs#selected) |
| [Get Selected HTML For Multiple Selectors](actions/get-selected-html-for-multiple-selectors.md) | `GET /selected-multiple` | [docs](https://webscraping.ai/docs#selected) |
