# Vistaly: Native API Reference

A consolidated summary of Vistaly's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://docs.vistaly.com/api-reference/introduction
- **API base URL:** `https://api.vistaly.com`

## Authentication

### API Key

Connect with a Vistaly API key used as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.vistaly.com/api-reference/system/auth-info-endpoint)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Card](actions/create-card.md) | `POST /beta/cards` | [docs](https://docs.vistaly.com/api-reference/cards/create-a-new-card) |
| [Delete Feedback](actions/delete-feedback.md) | `DELETE /v1/feedback/{feedbackId}` | [docs](https://docs.vistaly.com/api-reference/feedback/delete-feedback) |
| [Get Auth Info](actions/get-auth-info.md) | `GET /v1/auth/info` | [docs](https://docs.vistaly.com/api-reference/system/auth-info-endpoint) |
| [Get Card Context](actions/get-card-context.md) | `GET /beta/cards/{cardId}/context` | [docs](https://docs.vistaly.com/api-reference/cards/get-card-context) |
| [Get Card Details](actions/get-card-details.md) | `GET /beta/cards/{cardId}` | [docs](https://docs.vistaly.com/api-reference/cards/get-card-details) |
| [Get Interview Transcript](actions/get-interview-transcript.md) | `GET /v1/interviews/{interviewId}/transcript` | [docs](https://docs.vistaly.com/api-reference/interviews/get-interview-transcript) |
| [Health Check](actions/health-check.md) | `GET /v1/health` | [docs](https://docs.vistaly.com/api-reference/system/health-check-endpoint) |
| [List Card Comments](actions/list-card-comments.md) | `GET /beta/cards/{cardId}/comments` | [docs](https://docs.vistaly.com/api-reference/cards/list-comments-for-a-card) |
| [Search Cards](actions/search-cards.md) | `POST /beta/cards/search` | [docs](https://docs.vistaly.com/api-reference/cards/search-cards-using-semantic-search) |
| [Submit Bulk Metrics for Card](actions/submit-bulk-metrics-for-card.md) | `POST /v1/cards/{cardId}/metrics/bulk` | [docs](https://docs.vistaly.com/api-reference/cards/submit-bulk-metrics-for-a-card) |
| [Submit Interview Data](actions/submit-interview-data.md) | `POST /v1/interviews` | [docs](https://docs.vistaly.com/api-reference/interviews/submit-interview-data) |
| [Submit Metrics for Card](actions/submit-metrics-for-card.md) | `POST /v1/cards/{cardId}/metrics` | [docs](https://docs.vistaly.com/api-reference/cards/submit-metrics-for-a-card) |
| [Submit User Feedback](actions/submit-user-feedback.md) | `POST /v1/feedback` | [docs](https://docs.vistaly.com/api-reference/feedback/submit-user-feedback) |
| [Update Card](actions/update-card.md) | `PUT /beta/cards/{cardId}` | [docs](https://docs.vistaly.com/api-reference/cards/update-card) |
| [Update Card Parents](actions/update-card-parents.md) | `PUT /beta/cards/{cardId}/parents` | [docs](https://docs.vistaly.com/api-reference/cards/update-card-parents) |
