# BlockSurvey: Native API Reference

A consolidated summary of BlockSurvey's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://documents.blocksurvey.io/
- **API base URL:** `https://api3.blocksurvey.io`

## Authentication

### API Key

Use a BlockSurvey API key generated from Organization Settings to authenticate requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://documents.blocksurvey.io/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /contact/create-contact` | [docs](https://documents.blocksurvey.io/audience/create-contact) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contact/delete-contact` | [docs](https://documents.blocksurvey.io/audience/delete-contact) |
| [Get Contact](actions/get-contact.md) | `POST /contact/get-contact` | [docs](https://documents.blocksurvey.io/audience/get-contact) |
| [Get Survey Cut Off Date](actions/get-survey-cut-off-date.md) | `GET /v1/survey/cut_off_date` | [docs](https://documents.blocksurvey.io/survey/get-a-survey-cut-off-date) |
| [Get Survey Limit Maximum Response Count](actions/get-survey-limit-maximum-response-count.md) | `GET /v1/survey/limit_maximum_response_count` | [docs](https://documents.blocksurvey.io/survey/get-a-survey-limit-maximum-response-count) |
| [Get Survey Scheduled Start Date](actions/get-survey-scheduled-start-date.md) | `GET /v1/survey/scheduled_start_date` | [docs](https://documents.blocksurvey.io/survey/get-a-survey-scheduled-start-date) |
| [Get Survey Text Variable Value](actions/get-survey-text-variable-value.md) | `GET /v1/survey/text_variable_value` | [docs](https://documents.blocksurvey.io/survey/get-a-survey-text-variable-value) |
| [Update Contact](actions/update-contact.md) | `PUT /contact/update-contact` | [docs](https://documents.blocksurvey.io/audience/update-contact) |
| [Update Survey Cut Off Date](actions/update-survey-cut-off-date.md) | `POST /v1/survey/cut_off_date` | [docs](https://documents.blocksurvey.io/survey/update-a-survey-cut-off-date) |
| [Update Survey Limit Maximum Response Count](actions/update-survey-limit-maximum-response-count.md) | `POST /v1/survey/limit_maximum_response_count` | [docs](https://documents.blocksurvey.io/survey/update-a-survey-limit-maximum-response-count) |
| [Update Survey Scheduled Start Date](actions/update-survey-scheduled-start-date.md) | `POST /v1/survey/scheduled_start_date` | [docs](https://documents.blocksurvey.io/survey/update-a-survey-scheduled-start-date) |
| [Update Survey Text Variable Value](actions/update-survey-text-variable-value.md) | `POST /v1/survey/text_variable_value` | [docs](https://documents.blocksurvey.io/survey/update-a-survey-text-variable-value) |
