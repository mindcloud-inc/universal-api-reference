# Startquestion: Native API Reference

A consolidated summary of Startquestion's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://help.startquestion.com/en/collections/3120305-api-documentation
- **API base URL:** `https://www.startquestion.com/api/v2`

## Authentication

### OAuth 2.0 (Client Credentials)

Startquestion API v2 machine-to-machine OAuth2 flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://auth.startquestion.com/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `v2-all`.

A machine-to-machine flow is configured.

[Official authentication documentation](https://help.startquestion.com/en/articles/10906381-integration-with-power-bi)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–1000). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Respondent to Survey](actions/add-respondent-to-survey.md) | `GET /respondents/add` | [docs](https://help.startquestion.com/en/articles/5810169-respondents) |
| [Append Respondent Batch](actions/append-respondent-batch.md) | `POST /respondents/patch` | [docs](https://help.startquestion.com/en/articles/5810169-respondents) |
| [Create Batch Mailing](actions/create-batch-mailing.md) | `POST /mailing/batch` | [docs](https://help.startquestion.com/en/articles/5810255-mailing) |
| [Create Contact](actions/create-contact.md) | `GET /contacts/add` | [docs](https://help.startquestion.com/en/articles/5810000-contacts) |
| [Create Mailing](actions/create-mailing.md) | `POST /mailing/create` | [docs](https://help.startquestion.com/en/articles/5810255-mailing) |
| [Create Offline Contact](actions/create-offline-contact.md) | `GET /contacts/add-offline` | [docs](https://help.startquestion.com/en/articles/5810000-contacts) |
| [Create Respondent Batch](actions/create-respondent-batch.md) | `POST /respondents/batch` | [docs](https://help.startquestion.com/en/articles/5810169-respondents) |
| [Delete Respondent](actions/delete-respondent.md) | `GET /respondents/delete` | [docs](https://help.startquestion.com/en/articles/5810169-respondents) |
| [Download Result Attachment](actions/download-result-attachment.md) | `GET https://app.startquestion.com/api/v2/results/:surveyId/fill/:fillId/attachment/:questionId` | [docs](https://help.startquestion.com/en/articles/5810324-results) |
| [Get Respondent Batch](actions/get-respondent-batch.md) | `GET /respondents/batch` | [docs](https://help.startquestion.com/en/articles/5810169-respondents) |
| [Get Respondent Patch](actions/get-respondent-patch.md) | `GET /respondents/patch` | [docs](https://help.startquestion.com/en/articles/5810169-respondents) |
| [Get Response V2 by ID](actions/get-response-v2-by-id.md) | `GET /results/single-sheets/:id_survey` | [docs](https://help.startquestion.com/en/articles/5810324-results) |
| [Get Response V2 by Token](actions/get-response-v2-by-token.md) | `GET /results/single-sheets/:id_survey` | [docs](https://help.startquestion.com/en/articles/5810324-results) |
| [Get Response V3 by ID](actions/get-response-v3-by-id.md) | `GET https://www.startquestion.com/api/v3/results/single-sheets/:id_survey` | [docs](https://help.startquestion.com/en/articles/5810324-results) |
| [Get Response V3 by Token](actions/get-response-v3-by-token.md) | `GET https://www.startquestion.com/api/v3/results/single-sheets/:id_survey` | [docs](https://help.startquestion.com/en/articles/5810324-results) |
| [Get Result Metadata by Response ID](actions/get-result-metadata-by-response-id.md) | `GET /results/meta/:id_survey` | [docs](https://help.startquestion.com/en/articles/5810324-results) |
| [Get Result Metadata by Token](actions/get-result-metadata-by-token.md) | `GET /results/meta/:id_survey` | [docs](https://help.startquestion.com/en/articles/5810324-results) |
| [Get Results Metadata](actions/get-results-metadata.md) | `GET /results/meta/:id_survey` | [docs](https://help.startquestion.com/en/articles/5810324-results) |
| [Get Survey](actions/get-survey.md) | `GET /surveys/:id` | [docs](https://help.startquestion.com/en/articles/5810076-surveys) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://help.startquestion.com/en/articles/5810000-contacts) |
| [List Mailing Templates](actions/list-mailing-templates.md) | `GET /mailing/templates` | [docs](https://help.startquestion.com/en/articles/5810255-mailing) |
| [List Page Questions](actions/list-page-questions.md) | `GET /questions/:id_survey/:id_page` | [docs](https://help.startquestion.com/en/articles/5809873-questions) |
| [List Responses V2](actions/list-responses-v2.md) | `GET /results/single-sheets/:id_survey` | [docs](https://help.startquestion.com/en/articles/5810324-results) |
| [List Responses V3](actions/list-responses-v3.md) | `GET https://www.startquestion.com/api/v3/results/single-sheets/:id_survey` | [docs](https://help.startquestion.com/en/articles/5810324-results) |
| [List Survey Respondents](actions/list-survey-respondents.md) | `GET /respondents/:id_survey` | [docs](https://help.startquestion.com/en/articles/5810169-respondents) |
| [List Surveys](actions/list-surveys.md) | `GET /surveys` | [docs](https://help.startquestion.com/en/articles/5810076-surveys) |
| [Search Contacts](actions/search-contacts.md) | `GET /contacts/search` | [docs](https://help.startquestion.com/en/articles/5810000-contacts) |
| [Search Responses by External Key](actions/search-responses-by-external-key.md) | `GET /results/single-sheets/:id_survey` | [docs](https://help.startquestion.com/en/articles/5810324-results) |
| [Search Survey Respondents](actions/search-survey-respondents.md) | `GET /respondents/search/:id_survey` | [docs](https://help.startquestion.com/en/articles/5810169-respondents) |
| [Search Surveys](actions/search-surveys.md) | `GET /surveys/search` | [docs](https://help.startquestion.com/en/articles/5810076-surveys) |
