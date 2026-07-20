# Linguin AI: Native API Reference

A consolidated summary of Linguin AI's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://linguin.ai/api-docs/v2/
- **API base URL:** `https://api.linguin.ai`

## Authentication

### API Key

Authenticate with a Linguin AI API key sent as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://linguin.ai/api-docs/v2/)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Detect Language](actions/bulk-detect-language.md) | `POST /v2/bulk_detect/language` | [docs](https://linguin.ai/api-docs/v2/#bulk-language-detection) |
| [Bulk Detect Profanity](actions/bulk-detect-profanity.md) | `POST /v2/bulk_detect/profanity` | [docs](https://linguin.ai/api-docs/v2/#bulk-profanity-detection) |
| [Detect Language](actions/detect-language.md) | `POST /v2/detect/language` | [docs](https://linguin.ai/api-docs/v2/#single-language-detection) |
| [Detect Profanity](actions/detect-profanity.md) | `POST /v2/detect/profanity` | [docs](https://linguin.ai/api-docs/v2/#single-profanity-detection) |
| [Get Account Status](actions/get-account-status.md) | `GET /v2/status` | [docs](https://linguin.ai/api-docs/v2/#account-status) |
| [List Supported Languages](actions/list-supported-languages.md) | `GET /v2/languages` | [docs](https://linguin.ai/api-docs/v2/#list-of-supported-languages) |
