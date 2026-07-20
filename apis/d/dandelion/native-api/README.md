# Dandelion: Native API Reference

A consolidated summary of Dandelion's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://dandelion.eu/docs/api/
- **API base URL:** `https://api.dandelion.eu`

## Authentication

### API Key

Use a Dandelion API token sent as the required token query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://dandelion.eu/docs/api/)

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze Sentiment From HTML Fragment via HTTP GET](actions/analyze-sentiment-from-html-fragment-get.md) | `GET /datatxt/sent/v1` | [docs](https://dandelion.eu/docs/api/datatxt/sent/v1/) |
| [Analyze Sentiment From HTML Fragment via HTTP POST](actions/analyze-sentiment-from-html-fragment-post.md) | `POST /datatxt/sent/v1` | [docs](https://dandelion.eu/docs/api/datatxt/sent/v1/) |
| [Analyze Sentiment From HTML via HTTP GET](actions/analyze-sentiment-from-html-get.md) | `GET /datatxt/sent/v1` | [docs](https://dandelion.eu/docs/api/datatxt/sent/v1/) |
| [Analyze Sentiment From HTML via HTTP POST](actions/analyze-sentiment-from-html-post.md) | `POST /datatxt/sent/v1` | [docs](https://dandelion.eu/docs/api/datatxt/sent/v1/) |
| [Analyze Sentiment From Text via HTTP GET](actions/analyze-sentiment-from-text-get.md) | `GET /datatxt/sent/v1` | [docs](https://dandelion.eu/docs/api/datatxt/sent/v1/) |
| [Analyze Sentiment From Text via HTTP POST](actions/analyze-sentiment-from-text-post.md) | `POST /datatxt/sent/v1` | [docs](https://dandelion.eu/docs/api/datatxt/sent/v1/) |
| [Autocomplete Wikipedia Entities via HTTP GET](actions/autocomplete-wikipedia-entities-get.md) | `GET /datagraph/wikisearch/v1` | [docs](https://dandelion.eu/docs/api/datagraph/wikisearch/) |
| [Autocomplete Wikipedia Entities via HTTP POST](actions/autocomplete-wikipedia-entities-post.md) | `POST /datagraph/wikisearch/v1` | [docs](https://dandelion.eu/docs/api/datagraph/wikisearch/) |
| [Compare HTML Fragment Similarity via HTTP GET](actions/compare-html-fragment-similarity-get.md) | `GET /datatxt/sim/v1` | [docs](https://dandelion.eu/docs/api/datatxt/sim/v1/) |
| [Compare HTML Fragment Similarity via HTTP POST](actions/compare-html-fragment-similarity-post.md) | `POST /datatxt/sim/v1` | [docs](https://dandelion.eu/docs/api/datatxt/sim/v1/) |
| [Compare HTML Similarity via HTTP GET](actions/compare-html-similarity-get.md) | `GET /datatxt/sim/v1` | [docs](https://dandelion.eu/docs/api/datatxt/sim/v1/) |
| [Compare HTML Similarity via HTTP POST](actions/compare-html-similarity-post.md) | `POST /datatxt/sim/v1` | [docs](https://dandelion.eu/docs/api/datatxt/sim/v1/) |
| [Compare Text Similarity via HTTP GET](actions/compare-text-similarity-get.md) | `GET /datatxt/sim/v1` | [docs](https://dandelion.eu/docs/api/datatxt/sim/v1/) |
| [Compare Text Similarity via HTTP POST](actions/compare-text-similarity-post.md) | `POST /datatxt/sim/v1` | [docs](https://dandelion.eu/docs/api/datatxt/sim/v1/) |
| [Detect Language From HTML Fragment via HTTP GET](actions/detect-language-from-html-fragment-get.md) | `GET /datatxt/li/v1` | [docs](https://dandelion.eu/docs/api/datatxt/li/v1/) |
| [Detect Language From HTML Fragment via HTTP POST](actions/detect-language-from-html-fragment-post.md) | `POST /datatxt/li/v1` | [docs](https://dandelion.eu/docs/api/datatxt/li/v1/) |
| [Detect Language From HTML via HTTP GET](actions/detect-language-from-html-get.md) | `GET /datatxt/li/v1` | [docs](https://dandelion.eu/docs/api/datatxt/li/v1/) |
| [Detect Language From HTML via HTTP POST](actions/detect-language-from-html-post.md) | `POST /datatxt/li/v1` | [docs](https://dandelion.eu/docs/api/datatxt/li/v1/) |
| [Detect Language From Text via HTTP GET](actions/detect-language-from-text-get.md) | `GET /datatxt/li/v1` | [docs](https://dandelion.eu/docs/api/datatxt/li/v1/) |
| [Detect Language From Text via HTTP POST](actions/detect-language-from-text-post.md) | `POST /datatxt/li/v1` | [docs](https://dandelion.eu/docs/api/datatxt/li/v1/) |
| [Extract Entities From HTML Fragment via HTTP GET](actions/extract-entities-from-html-fragment-get.md) | `GET /datatxt/nex/v1` | [docs](https://dandelion.eu/docs/api/datatxt/nex/v1/) |
| [Extract Entities From HTML Fragment via HTTP POST](actions/extract-entities-from-html-fragment-post.md) | `POST /datatxt/nex/v1` | [docs](https://dandelion.eu/docs/api/datatxt/nex/v1/) |
| [Extract Entities From HTML via HTTP GET](actions/extract-entities-from-html-get.md) | `GET /datatxt/nex/v1` | [docs](https://dandelion.eu/docs/api/datatxt/nex/v1/) |
| [Extract Entities From HTML via HTTP POST](actions/extract-entities-from-html-post.md) | `POST /datatxt/nex/v1` | [docs](https://dandelion.eu/docs/api/datatxt/nex/v1/) |
| [Extract Entities From Text via HTTP GET](actions/extract-entities-from-text-get.md) | `GET /datatxt/nex/v1` | [docs](https://dandelion.eu/docs/api/datatxt/nex/v1/) |
| [Extract Entities From Text via HTTP POST](actions/extract-entities-from-text-post.md) | `POST /datatxt/nex/v1` | [docs](https://dandelion.eu/docs/api/datatxt/nex/v1/) |
| [Search Wikipedia Entities via HTTP GET](actions/search-wikipedia-entities-get.md) | `GET /datagraph/wikisearch/v1` | [docs](https://dandelion.eu/docs/api/datagraph/wikisearch/) |
| [Search Wikipedia Entities via HTTP POST](actions/search-wikipedia-entities-post.md) | `POST /datagraph/wikisearch/v1` | [docs](https://dandelion.eu/docs/api/datagraph/wikisearch/) |
