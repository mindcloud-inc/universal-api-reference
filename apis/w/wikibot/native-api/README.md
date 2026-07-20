# Wikibot: Native API Reference

A consolidated summary of Wikibot's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://wikibot.pro/docs/api
- **API base URL:** `https://api.wikibot.pro/api`

## Authentication

### API Key

Connect Wikibot using the API key from your Wikibot account.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://wikibot.pro/docs/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Anonymize Text](actions/anonymize-text.md) | `POST /bot/anonymize` | [docs](https://wikibot.pro/docs/api/anonymize) |
| [Ask Question](actions/ask-question.md) | `POST /bot/ask` | [docs](https://wikibot.pro/docs/api/ask) |
| [Ask Question With Query Parameters](actions/ask-question-with-query-parameters.md) | `GET /bot/ask` | [docs](https://wikibot.pro/docs/api/ask-get) |
| [Create Knowledge Base](actions/create-knowledge-base.md) | `POST /bot/kb/create` | [docs](https://wikibot.pro/docs/api/kb-create) |
| [Deanonymize Text](actions/deanonymize-text.md) | `POST /bot/deanonymize` | [docs](https://wikibot.pro/docs/api/deanonymize) |
| [Get Knowledge Base](actions/get-knowledge-base.md) | `GET /bot/kb` | [docs](https://wikibot.pro/docs/api/kb) |
| [List Agents](actions/list-agents.md) | `GET /bot/agents` | [docs](https://wikibot.pro/docs/api/agents) |
| [Search Knowledge Base](actions/search-knowledge-base.md) | `GET /bot/search` | [docs](https://wikibot.pro/docs/api/search) |
| [Set Webhook URL](actions/set-webhook-url.md) | `POST /bot/set-webhook-url` | [docs](https://wikibot.pro/docs/api/set-webhook-url) |
| [Upload Knowledge Base Document](actions/upload-knowledge-base-document.md) | `POST /bot/kb/upload-file` | [docs](https://wikibot.pro/docs/api/kb-upload) |
