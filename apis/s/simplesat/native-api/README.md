# Simplesat: Native API Reference

A consolidated summary of Simplesat's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://developer.simplesat.io/api
- **OpenAPI specification:** https://developer.simplesat.io/api/Simplesat%20API%20(v1)%20OpenAPI.yaml
- **API base URL:** `https://api.simplesat.io`

## Authentication

### API Key

Connect with a Simplesat API key sent only in the X-Simplesat-Token header.

Send these headers with each API request:

```http
X-Simplesat-Token: <apiKey>
```

[Official authentication documentation](https://developer.simplesat.io/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 100; maximum 250). Use `page` in the query string to choose the page; numbering starts at 1. Follow the complete next-page URL returned by the API.

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Upsert Customers](actions/bulk-upsert-customers.md) | `POST /api/v1/customers/bulk` | [docs](https://developer.simplesat.io/api) |
| [Create or Update Customer](actions/create-or-update-customer.md) | `POST /api/v1/customers` | [docs](https://developer.simplesat.io/api) |
| [Create or Update Response](actions/create-or-update-response.md) | `POST /api/v1/responses/create-or-update` | [docs](https://developer.simplesat.io/api) |
| [Create or Update Team Member](actions/create-or-update-team-member.md) | `POST /api/v1/team-members` | [docs](https://developer.simplesat.io/api) |
| [Get Answer](actions/get-answer.md) | `GET /api/v1/answers/:answer_id` | [docs](https://developer.simplesat.io/api) |
| [Get Customer](actions/get-customer.md) | `GET /api/v1/customers/:customer_id` | [docs](https://developer.simplesat.io/api) |
| [Get Response](actions/get-response.md) | `GET /api/v1/responses/:response_id` | [docs](https://developer.simplesat.io/api) |
| [Get Team Member](actions/get-team-member.md) | `GET /api/v1/team-members/:team_member_id` | [docs](https://developer.simplesat.io/api) |
| [List Customers](actions/list-customers.md) | `GET /api/v1/customers` | [docs](https://developer.simplesat.io/api) |
| [List Questions](actions/list-questions.md) | `GET /api/v1/questions` | [docs](https://developer.simplesat.io/api) |
| [List Surveys](actions/list-surveys.md) | `GET /api/v1/surveys` | [docs](https://developer.simplesat.io/api) |
| [Search Answers](actions/search-answers.md) | `POST /api/v1/answers/search` | [docs](https://developer.simplesat.io/api) |
| [Search Responses](actions/search-responses.md) | `POST /api/v1/responses/search` | [docs](https://developer.simplesat.io/api) |
| [Send Survey by Email](actions/send-survey-by-email.md) | `POST /api/v1/surveys/:survey_token/email` | [docs](https://developer.simplesat.io/api) |
| [Update Answer](actions/update-answer.md) | `PUT /api/v1/answers/:answer_id` | [docs](https://developer.simplesat.io/api) |
| [Update Customer](actions/update-customer.md) | `PUT /api/v1/customers/:customer_id` | [docs](https://developer.simplesat.io/api) |
| [Update Response](actions/update-response.md) | `PUT /api/v1/responses/:response_id/update` | [docs](https://developer.simplesat.io/api) |
