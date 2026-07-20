# Trustmary: Native API Reference

A consolidated summary of Trustmary's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://help.trustmary.com/api
- **API base URL:** `https://api.trustmary.io/v1`

## Authentication

### API Key

Retrieves widgets from Trustmary.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.trustmary.com/en/article/api-authentication-developers-11uji38)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create or Update Contact](actions/create-or-update-contact.md) | `POST /contacts` | [docs](https://help.trustmary.com/api#/paths/~1contacts/post) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://help.trustmary.com/api#/paths/~1webhooks/post) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts` | [docs](https://help.trustmary.com/api#/paths/~1contacts/delete) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:webhookId` | [docs](https://help.trustmary.com/api#/paths/~1webhooks~1{webhook_id}/delete) |
| [Get Survey Information](actions/get-survey-information.md) | `GET /survey/:surveyId` | [docs](https://help.trustmary.com/api#/paths/~1survey~1{surveyId}/get) |
| [Get Webhook Example Payload](actions/get-webhook-example-payload.md) | `GET /webhooks/example` | [docs](https://help.trustmary.com/api#/paths/~1webhooks~1example/get) |
| [List Contact Lists](actions/list-contact-lists.md) | `GET /lists` | [docs](https://help.trustmary.com/api#/paths/~1lists/get) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://help.trustmary.com/api#/paths/~1contacts/get) |
| [List Embeds](actions/list-embeds.md) | `GET /embeds` | [docs](https://help.trustmary.com/api#/paths/~1embeds/get) |
| [List Experiments](actions/list-experiments.md) | `GET /experiments` | [docs](https://help.trustmary.com/api#/paths/~1experiments/get) |
| [List Survey Responses](actions/list-survey-responses.md) | `GET /survey/:surveyId/responses` | [docs](https://help.trustmary.com/api#/paths/~1survey~1{survey_id}~1responses/get) |
| [List Surveys](actions/list-surveys.md) | `GET /surveys` | [docs](https://help.trustmary.com/api#/paths/~1surveys/get) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://help.trustmary.com/api#/paths/~1webhooks/get) |
| [List Widgets](actions/list-widgets.md) | `GET /widgets` | [docs](https://help.trustmary.com/api#/paths/~1widgets/get) |
| [Test API Key](actions/test-api-key.md) | `GET /test` | [docs](https://help.trustmary.com/api#/paths/~1test/get) |
