# Evalandgo: Native API Reference

A consolidated summary of Evalandgo's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://app.evalandgo.com/api/docs/v3
- **API base URL:** `https://app.evalandgo.com`

## Authentication

### Bearer API Key

Authenticate Evalandgo API requests with a bearer API key from the API & Webhook settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.evalandgo.com/portal/fr/kb/articles/qu-est-ce-que-l-api-evalandgo-et-%C3%A0-quoi-sert-elle)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | `POST /api/v3/contacts` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1contacts/post) |
| [Create Form Response](actions/create-form-response.md) | `POST /api/v3/responses/form` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1responses~1form/post) |
| [Create Multiple Response](actions/create-multiple-response.md) | `POST /api/v3/responses/multiple` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1responses~1multiple/post) |
| [Create Respondent](actions/create-respondent.md) | `POST /api/v3/respondents` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1respondents/post) |
| [Create Text Response](actions/create-text-response.md) | `POST /api/v3/responses/text` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1responses~1text/post) |
| [Create Unique Response](actions/create-unique-response.md) | `POST /api/v3/responses/unique` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1responses~1unique/post) |
| [Create Webhook](actions/create-webhook.md) | `POST /api/v3/webhooks` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1webhooks/post) |
| [Download Question Drawing Files](actions/download-question-drawing-files.md) | `GET /api/v3/questions/drawing/:id/download/:format` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1questions~1drawing~1{id}~1download~1{format}/get) |
| [Download Question Upload Files](actions/download-question-upload-files.md) | `GET /api/v3/questions/upload/:id/download` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1questions~1upload~1{id}~1download/get) |
| [List Contact Respondents](actions/list-contact-respondents.md) | `GET /api/v3/contacts/:contactId/respondents` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1contacts~1{contactId}~1respondents/get) |
| [List Contacts](actions/list-contacts.md) | `GET /api/v3/contacts` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1contacts/get) |
| [List Fields](actions/list-fields.md) | `GET /api/v3/fields` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1fields/get) |
| [List Groups](actions/list-groups.md) | `GET /api/v3/groups` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1groups/get) |
| [List Question Responses](actions/list-question-responses.md) | `GET /api/v3/questions/:questionId/responses` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1questions~1{questionId}~1responses/get) |
| [List Questionnaire Questions](actions/list-questionnaire-questions.md) | `GET /api/v3/questionnaires/:id/questions` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1questionnaires~1{id}~1questions/get) |
| [List Questionnaire Webhooks](actions/list-questionnaire-webhooks.md) | `GET /api/v3/questionnaires/:questionnaireId/webhooks` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1questionnaires~1{questionnaireId}~1webhooks/get) |
| [List Questionnaires](actions/list-questionnaires.md) | `GET /api/v3/questionnaires` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1questionnaires/get) |
| [List Respondent Responses](actions/list-respondent-responses.md) | `GET /api/v3/respondents/:respondentId/responses` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1respondents~1{respondentId}~1responses/get) |
| [List Tags](actions/list-tags.md) | `GET /api/v3/tags` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1tags/get) |
| [Replace Webhook](actions/replace-webhook.md) | `PUT /api/v3/webhooks/:id` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1webhooks~1{id}/put) |
| [Retrieve Contact](actions/retrieve-contact.md) | `GET /api/v3/contacts/:id` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1contacts~1{id}/get) |
| [Retrieve Form Question](actions/retrieve-form-question.md) | `GET /api/v3/questions/form/:id` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1questions~1form~1{id}/get) |
| [Retrieve Form Response](actions/retrieve-form-response.md) | `GET /api/v3/responses/form/:id` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1responses~1form~1{id}/get) |
| [Retrieve Group](actions/retrieve-group.md) | `GET /api/v3/groups/:id` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1groups~1{id}/get) |
| [Retrieve Questionnaire](actions/retrieve-questionnaire.md) | `GET /api/v3/questionnaires/:id` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1questionnaires~1{id}/get) |
| [Retrieve Respondent Response](actions/retrieve-respondent-response.md) | `GET /api/v3/respondents/:respondentId/responses/:id` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1respondents~1{respondentId}~1responses~1{id}/get) |
| [Update Form Response Input](actions/update-form-response-input.md) | `PUT /api/v3/responses/form/:responseId/inputs/:inputId` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1responses~1form~1{responseId}~1inputs~1{inputId}/put) |
| [Update Multiple Response](actions/update-multiple-response.md) | `PUT /api/v3/responses/multiple/:id` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1responses~1multiple~1{id}/put) |
| [Update Text Response](actions/update-text-response.md) | `PUT /api/v3/responses/text/:id` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1responses~1text~1{id}/put) |
| [Update Unique Response](actions/update-unique-response.md) | `PUT /api/v3/responses/unique/:id` | [docs](https://app.evalandgo.com/api/docs/v3?format=json#/paths/~1api~1v3~1responses~1unique~1{id}/put) |
