# TranslatePlus: Native API Reference

A consolidated summary of TranslatePlus's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://docs.translateplus.io
- **OpenAPI specification:** https://api.translateplus.io/openapi.json
- **API base URL:** `https://api.translateplus.io`

## Authentication

### API Key

Connect using your TranslatePlus API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.translateplus.io/getting-started/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Translate Text](actions/batch-translate-text.md) | `POST /v2/translate/batch` | [docs](https://docs.translateplus.io/reference/v2/translation/batch-translate) |
| [Create I18n Translation Job](actions/create-i18n-translation-job.md) | `POST /v2/translate/i18n` | [docs](https://docs.translateplus.io/reference/v2/i18n/i18n-create-job) |
| [Delete I18n Job](actions/delete-i18n-job.md) | `DELETE /v2/translate/i18n/jobs/{job_id}` | [docs](https://docs.translateplus.io/reference/v2/i18n/i18n-delete-job) |
| [Detect Language](actions/detect-language.md) | `POST /v2/language_detect` | [docs](https://docs.translateplus.io/reference/v2/language/detect-language) |
| [Download I18n File](actions/download-i18n-file.md) | `GET /v2/translate/i18n/jobs/{job_id}/download` | [docs](https://docs.translateplus.io/reference/v2/i18n/i18n-download) |
| [Get Account Summary](actions/get-account-summary.md) | `GET /v2/account/summary` | [docs](https://docs.translateplus.io/reference/v2/account/account-summary) |
| [Get I18n Job Status](actions/get-i18n-job-status.md) | `GET /v2/translate/i18n/jobs/{job_id}/status` | [docs](https://docs.translateplus.io/reference/v2/i18n/i18n-job-status) |
| [Get Supported Languages](actions/get-supported-languages.md) | `GET /v2/supported-languages` | [docs](https://docs.translateplus.io/reference/v2/language/supported-languages) |
| [Health Check](actions/health-check.md) | `GET /health` | [docs](https://docs.translateplus.io/reference/v2/account/health) |
| [List I18n Jobs](actions/list-i18n-jobs.md) | `GET /v2/translate/i18n/jobs` | [docs](https://docs.translateplus.io/reference/v2/i18n/i18n-list-jobs) |
| [Translate Email](actions/translate-email.md) | `POST /v2/translate/email` | [docs](https://docs.translateplus.io/reference/v2/translation/translate-email) |
| [Translate HTML](actions/translate-html.md) | `POST /v2/translate/html` | [docs](https://docs.translateplus.io/reference/v2/translation/translate-html) |
| [Translate Subtitles](actions/translate-subtitles.md) | `POST /v2/translate/subtitles` | [docs](https://docs.translateplus.io/reference/v2/translation/translate-subtitles) |
| [Translate Text](actions/translate-text.md) | `POST /v2/translate` | [docs](https://docs.translateplus.io/reference/v2/translation/translate) |
