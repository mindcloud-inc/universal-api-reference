# TgBooster: Native API Reference

A consolidated summary of TgBooster's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://tgbooster.gitbook.io/tgbooster/api/api-metody
- **API base URL:** `https://api.tgbooster.ru/api`

## Authentication

### API Key

Use a TgBooster API key as a Bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://tgbooster.gitbook.io/tgbooster/api/autentifikaciya)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Reports](actions/get-reports.md) | `POST /cabinet/{CabinetId}/reports` | [docs](https://tgbooster.gitbook.io/tgbooster/api/api-metody#poluchenie-otchetov) |
| [List Cabinets](actions/list-cabinets.md) | `POST /cabinets` | [docs](https://tgbooster.gitbook.io/tgbooster/api/api-metody#poluchenie-spiska-kabinetov) |
| [List Campaigns](actions/list-campaigns.md) | `POST /cabinet/{CabinetId}/companies` | [docs](https://tgbooster.gitbook.io/tgbooster/api/api-metody#poluchenie-spiska-kampanii-s-vozmozhnostyu-filtracii-statistiki) |
