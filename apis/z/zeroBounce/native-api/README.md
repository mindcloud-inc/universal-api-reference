# ZeroBounce: Native API Reference

A consolidated summary of ZeroBounce's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://www.zerobounce.net/docs
- **API base URL:** `https://api.zerobounce.net`

## Authentication

### API Key

Connect ZeroBounce with an API key from your ZeroBounce account.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.zerobounce.net/docs/api-dashboard#Keys_Management)

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Domain Search File Status](actions/bulk-domain-search-file-status.md) | `GET https://bulkapi.zerobounce.net/domain-search/filestatus` | [docs](https://www.zerobounce.net/docs/domain-search-api/bulk-domain-search-api/file-status) |
| [Bulk Domain Search Get File](actions/bulk-domain-search-get-file.md) | `GET https://bulkapi.zerobounce.net/domain-search/getfile` | [docs](https://www.zerobounce.net/docs/domain-search-api/bulk-domain-search-api/get-file) |
| [Bulk Find Email File Status](actions/bulk-find-email-file-status.md) | `GET https://bulkapi.zerobounce.net/email-finder/filestatus` | [docs](https://www.zerobounce.net/docs/email-finder-api/bulk-email-finder-api/bulk-file-status) |
| [Bulk Find Email Get File](actions/bulk-find-email-get-file.md) | `GET https://bulkapi.zerobounce.net/email-finder/getfile` | [docs](https://www.zerobounce.net/docs/email-finder-api/bulk-email-finder-api/bulk-get-file) |
| [Domain Search](actions/domain-search.md) | `GET /v2/guessformat` | [docs](https://www.zerobounce.net/docs/domain-search-api) |
| [Find Email](actions/find-email.md) | `GET /v2/guessformat` | [docs](https://www.zerobounce.net/docs/email-finder-api) |
| [Get Activity Data](actions/get-activity-data.md) | `GET /v2/activity` | [docs](https://www.zerobounce.net/docs/activity-data-api) |
| [Get API Usage](actions/get-api-usage.md) | `GET /v2/getapiusage` | [docs](https://www.zerobounce.net/docs/email-validation-api-quickstart/v2-get-api-usage) |
| [Get Credit Balance](actions/get-credit-balance.md) | `GET /v2/getcredits` | [docs](https://www.zerobounce.net/docs/email-validation-api-quickstart/v2-credit-balance) |
| [Get Evaluated List Status](actions/get-evaluated-list-status.md) | `GET https://bulkapi.zerobounce.net/v2/listevaluator/:file_id/` | [docs](https://www.zerobounce.net/docs/list-evaluator-api) |
| [Get Scoring File](actions/get-scoring-file.md) | `GET https://bulkapi.zerobounce.net/v2/scoring/getfile` | [docs](https://www.zerobounce.net/docs/ai-scoring-api) |
| [Get Scoring File Status](actions/get-scoring-file-status.md) | `GET https://bulkapi.zerobounce.net/v2/scoring/filestatus` | [docs](https://www.zerobounce.net/docs/ai-scoring-api) |
| [Get Validation File](actions/get-validation-file.md) | `GET https://bulkapi.zerobounce.net/v2/getfile` | [docs](https://www.zerobounce.net/docs/email-validation-api-quickstart/v2-get-file) |
| [Get Validation File Status](actions/get-validation-file-status.md) | `GET https://bulkapi.zerobounce.net/v2/filestatus` | [docs](https://www.zerobounce.net/docs/email-validation-api-quickstart/v2-file-status) |
| [List Validation Filters](actions/list-validation-filters.md) | `GET /v2/filters/list` | [docs](https://www.zerobounce.net/docs/email-validation-api-quickstart/v2-allowlist-and-blocklist) |
| [Score Email](actions/score-email.md) | `GET /v2/scoring` | [docs](https://www.zerobounce.net/docs/ai-scoring-api/single-email-scoring) |
| [Validate Email](actions/validate-email.md) | `GET /v2/validate` | [docs](https://www.zerobounce.net/docs/email-validation-api-quickstart/v2-validate-emails) |
| [Validate Email Batch](actions/validate-email-batch.md) | `POST /v2/validatebatch` | [docs](https://www.zerobounce.net/docs/email-validation-api-quickstart/v2-batch-validate-emails) |
