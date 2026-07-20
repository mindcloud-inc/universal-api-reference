# LLMLayer: Native API Reference

A consolidated summary of LLMLayer's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://docs.llmlayer.ai/api-reference/introduction
- **OpenAPI specification:** https://docs.llmlayer.ai/api-reference/openapi.json
- **API base URL:** `https://api.llmlayer.dev`

## Authentication

### LLMLayer API Key

Use your LLMLayer API key. Runtime requests send it as Authorization: Bearer <api_key>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.llmlayer.ai/api-reference/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Answer in HTML](actions/answer-in-html.md) | `POST /api/v2/answer` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/answer) |
| [Answer in JSON](actions/answer-in-json.md) | `POST /api/v2/answer` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/answer) |
| [Answer in Markdown](actions/answer-in-markdown.md) | `POST /api/v2/answer` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/answer) |
| [Answer in Spanish](actions/answer-in-spanish.md) | `POST /api/v2/answer` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/answer) |
| [Answer News Question](actions/answer-news-question.md) | `POST /api/v2/answer` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/answer) |
| [Answer Question](actions/answer-question.md) | `POST /api/v2/answer` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/answer) |
| [Answer with Domain Filter](actions/answer-with-domain-filter.md) | `POST /api/v2/answer` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/answer) |
| [Answer with Images](actions/answer-with-images.md) | `POST /api/v2/answer` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/answer) |
| [Answer with Sources](actions/answer-with-sources.md) | `POST /api/v2/answer` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/answer) |
| [Capture Website Screenshot](actions/capture-website-screenshot.md) | `POST /api/v2/scrape` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/scrape) |
| [Crawl Website](actions/crawl-website.md) | `POST /api/v2/crawl_stream` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/crawl) |
| [Crawl Website Deep](actions/crawl-website-deep.md) | `POST /api/v2/crawl_stream` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/crawl) |
| [Crawl Website Main Content](actions/crawl-website-main-content.md) | `POST /api/v2/crawl_stream` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/crawl) |
| [Extract PDF Content](actions/extract-pdf-content.md) | `POST /api/v2/get_pdf_content` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/scrape-pdf) |
| [Fast Answer](actions/fast-answer.md) | `POST /api/v2/answer` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/answer) |
| [Get YouTube Transcript](actions/get-youtube-transcript.md) | `POST /api/v2/youtube_transcript` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/youtube-transcript) |
| [Get YouTube Transcript by Language](actions/get-youtube-transcript-by-language.md) | `POST /api/v2/youtube_transcript` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/youtube-transcript) |
| [Map Website URLs](actions/map-website-urls.md) | `POST /api/v2/map` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/map) |
| [Map Website with Subdomains](actions/map-website-with-subdomains.md) | `POST /api/v2/map` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/map) |
| [Scrape Main Content Markdown](actions/scrape-main-content-markdown.md) | `POST /api/v2/scrape` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/scrape) |
| [Scrape Rich Content](actions/scrape-rich-content.md) | `POST /api/v2/scrape` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/scrape) |
| [Scrape Website HTML](actions/scrape-website-html.md) | `POST /api/v2/scrape` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/scrape) |
| [Scrape Website Markdown](actions/scrape-website-markdown.md) | `POST /api/v2/scrape` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/scrape) |
| [Search Images](actions/search-images.md) | `POST /api/v2/web_search` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/web-search) |
| [Search News](actions/search-news.md) | `POST /api/v2/web_search` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/web-search) |
| [Search Scholar](actions/search-scholar.md) | `POST /api/v2/web_search` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/web-search) |
| [Search Shopping](actions/search-shopping.md) | `POST /api/v2/web_search` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/web-search) |
| [Search Videos](actions/search-videos.md) | `POST /api/v2/web_search` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/web-search) |
| [Search Web](actions/search-web.md) | `POST /api/v2/web_search` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/web-search) |
| [Search Web with Domain Filter](actions/search-web-with-domain-filter.md) | `POST /api/v2/web_search` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/web-search) |
| [Search Website URLs](actions/search-website-urls.md) | `POST /api/v2/map` | [docs](https://docs.llmlayer.ai/api-reference/endpoint/map) |
