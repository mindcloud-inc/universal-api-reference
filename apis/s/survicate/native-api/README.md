# Survicate: Native API Reference

A consolidated summary of Survicate's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://developers.survicate.com/data-export/
- **OpenAPI specification:** https://developers.survicate.com/openapi/data-export_v2.yaml
- **API base URL:** `https://data-api.survicate.com/v2`

## Authentication

### API Key

Authenticate to Survicate Data Export API with the API key from Surveys Settings -> Access Keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.survicate.com/data-export/setup/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The next-page cursor is read from `pagination_data.next_url`.

## Pagination

Use `items_per_page` in the query string to set the page size (default 20; accepted range 1–100).

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Personal Data By Email](actions/delete-personal-data-by-email.md) | `DELETE /personal-data` | [docs](https://developers.survicate.com/data-export/personal-data/#delete-personal-data-by-email) |
| [Get Personal Data Counters](actions/get-personal-data-counters.md) | `GET /personal-data` | [docs](https://developers.survicate.com/data-export/personal-data/#get-personal-data-counters) |
| [Get Response](actions/get-response.md) | `GET /surveys/:survey_id/responses/:response_uuid` | [docs](https://developers.survicate.com/data-export/response/#retrieve-a-response) |
| [Get Survey](actions/get-survey.md) | `GET /surveys/:survey_id` | [docs](https://developers.survicate.com/data-export/survey/#retrieve-survey-information) |
| [List Respondent Attributes](actions/list-respondent-attributes.md) | `GET /respondents/:respondent_uuid/attributes` | [docs](https://developers.survicate.com/data-export/respondent/#list-respondents-attributes) |
| [List Respondent Responses](actions/list-respondent-responses.md) | `GET /respondents/:respondent_uuid/responses` | [docs](https://developers.survicate.com/data-export/respondent/#list-respondents-responses) |
| [List Survey Questions](actions/list-survey-questions.md) | `GET /surveys/:survey_id/questions` | [docs](https://developers.survicate.com/data-export/survey/#list-questions) |
| [List Survey Responses](actions/list-survey-responses.md) | `GET /surveys/:survey_id/responses` | [docs](https://developers.survicate.com/data-export/response/#list-all-responses) |
| [List Surveys](actions/list-surveys.md) | `GET /surveys` | [docs](https://developers.survicate.com/data-export/survey/#list-all-surveys) |
