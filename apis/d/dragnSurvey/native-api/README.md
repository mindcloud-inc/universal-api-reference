# Drag'n Survey: Native API Reference

A consolidated summary of Drag'n Survey's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developer.dragnsurvey.com
- **API base URL:** `https://developer.dragnsurvey.com/api/v2.0.0`

## Authentication

### Bearer API Token

Authenticate Drag'n Survey requests with a personal API token sent as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.dragnsurvey.com/api_token)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Collector Custom Links](actions/create-collector-custom-links.md) | `POST collectors/:collectorId/authenticate` | [docs](https://developer.dragnsurvey.com) |
| [Create Survey Collector](actions/create-survey-collector.md) | `POST surveys/:surveyId/collectors` | [docs](https://developer.dragnsurvey.com) |
| [Delete Collector](actions/delete-collector.md) | `DELETE collectors/:collectorId` | [docs](https://developer.dragnsurvey.com) |
| [Delete Respondent](actions/delete-respondent.md) | `DELETE respondents/:respondentId` | [docs](https://developer.dragnsurvey.com) |
| [Get Collector](actions/get-collector.md) | `GET collectors/:collectorId` | [docs](https://developer.dragnsurvey.com) |
| [Get Human Readable Respondent Responses](actions/get-human-readable-respondent-responses.md) | `GET respondents/:respondentId/responses` | [docs](https://developer.dragnsurvey.com) |
| [Get Page](actions/get-page.md) | `GET pages/:pageId` | [docs](https://developer.dragnsurvey.com) |
| [Get Question Definition](actions/get-question-definition.md) | `GET components/:componentId` | [docs](https://developer.dragnsurvey.com) |
| [Get Report](actions/get-report.md) | `GET reports/:reportId` | [docs](https://developer.dragnsurvey.com) |
| [Get Respondent Responses](actions/get-respondent-responses.md) | `GET respondents/:respondentId` | [docs](https://developer.dragnsurvey.com) |
| [Get Webhook](actions/get-webhook.md) | `GET webhooks/:webhookId` | [docs](https://developer.dragnsurvey.com) |
| [List Survey Collectors](actions/list-survey-collectors.md) | `GET surveys/:surveyId/collectors` | [docs](https://developer.dragnsurvey.com) |
| [List Survey Respondent IDs](actions/list-survey-respondent-ids.md) | `GET surveys/:surveyId/respondents` | [docs](https://developer.dragnsurvey.com) |
| [List Survey Respondent IDs Paginated](actions/list-survey-respondent-ids-paginated.md) | `GET surveys/:surveyId/respondents/paginated` | [docs](https://developer.dragnsurvey.com) |
| [List Surveys](actions/list-surveys.md) | `GET /surveys` | [docs](https://developer.dragnsurvey.com) |
| [List Webhooks](actions/list-webhooks.md) | `GET webhooks` | [docs](https://developer.dragnsurvey.com) |
| [Retrieve Question Responses](actions/retrieve-question-responses.md) | `GET components/:componentId/responses` | [docs](https://developer.dragnsurvey.com) |
| [Subscribe to Webhook](actions/subscribe-to-webhook.md) | `POST webhooks` | [docs](https://developer.dragnsurvey.com) |
| [Unsubscribe from Webhook](actions/unsubscribe-from-webhook.md) | `DELETE webhooks/:webhookId` | [docs](https://developer.dragnsurvey.com) |
| [Update Collector](actions/update-collector.md) | `PATCH collectors/:collectorId` | [docs](https://developer.dragnsurvey.com) |
