# TXT Werk: Native API Reference

A consolidated summary of TXT Werk's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://services.txtwerk.de/ws/documentation/index
- **API base URL:** `https://api.txtwerk.de`

## Authentication

### API Key

Authenticate requests with your TXTWerk API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://services.txtwerk.de/ws/documentation/index)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze Annotated Entities](actions/analyze-annotated-entities.md) | `POST /rest/txt/analyzer` | [docs](https://services.txtwerk.de/ws/documentation/showRequest) |
| [Analyze Entity Candidates](actions/analyze-entity-candidates.md) | `POST /rest/txt/analyzer` | [docs](https://services.txtwerk.de/ws/documentation/showRequest) |
| [Analyze HTML Article Authors](actions/analyze-html-article-authors.md) | `POST /rest/txt/analyzer` | [docs](https://services.txtwerk.de/ws/documentation/showRequest) |
| [Analyze HTML Article Bundle](actions/analyze-html-article-bundle.md) | `POST /rest/txt/analyzer` | [docs](https://services.txtwerk.de/ws/documentation/showRequest) |
| [Analyze Metadata-Enriched Entities](actions/analyze-metadata-enriched-entities.md) | `POST /rest/txt/analyzer` | [docs](https://services.txtwerk.de/ws/documentation/showRequest) |
| [Analyze Named Entities](actions/analyze-named-entities.md) | `POST /rest/txt/analyzer` | [docs](https://services.txtwerk.de/ws/documentation/showRequest) |
| [Analyze Text](actions/analyze-text.md) | `POST /rest/txt/analyzer` | [docs](https://services.txtwerk.de/ws/documentation/showRequest) |
| [Analyze Top Entities](actions/analyze-top-entities.md) | `POST /rest/txt/analyzer` | [docs](https://services.txtwerk.de/ws/documentation/showRequest) |
| [Analyze Weighted Document Bundle](actions/analyze-weighted-document-bundle.md) | `POST /rest/txt/analyzer` | [docs](https://services.txtwerk.de/ws/documentation/showRequest) |
| [Classify Categories](actions/classify-categories.md) | `POST /rest/txt/analyzer` | [docs](https://services.txtwerk.de/ws/documentation/showRequest) |
| [Extract Dates](actions/extract-dates.md) | `POST /rest/txt/analyzer` | [docs](https://services.txtwerk.de/ws/documentation/showRequest) |
| [Extract Lexicon Entities](actions/extract-lexicon-entities.md) | `POST /rest/txt/analyzer` | [docs](https://services.txtwerk.de/ws/documentation/showRequest) |
| [Extract Lexicon Tags](actions/extract-lexicon-tags.md) | `POST /rest/txt/analyzer` | [docs](https://services.txtwerk.de/ws/documentation/showRequest) |
| [Extract Measures](actions/extract-measures.md) | `POST /rest/txt/analyzer` | [docs](https://services.txtwerk.de/ws/documentation/showRequest) |
| [Extract NER Entities](actions/extract-ner-entities.md) | `POST /rest/txt/analyzer` | [docs](https://services.txtwerk.de/ws/documentation/showRequest) |
| [Extract Tags](actions/extract-tags.md) | `POST /rest/txt/analyzer` | [docs](https://services.txtwerk.de/ws/documentation/showRequest) |
| [Extract Tags With Title And Teaser](actions/extract-tags-with-title-and-teaser.md) | `POST /rest/txt/analyzer` | [docs](https://services.txtwerk.de/ws/documentation/showRequest) |
| [Generate Fingerprints](actions/generate-fingerprints.md) | `POST /rest/txt/analyzer` | [docs](https://services.txtwerk.de/ws/documentation/showRequest) |
