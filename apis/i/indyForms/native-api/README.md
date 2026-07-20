# IndyForms: Native API Reference

A consolidated summary of IndyForms's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://api.indyforms.com/swagger/index.html?urls.primaryName=Indyforms+Public+Api+v2
- **OpenAPI specification:** https://api.indyforms.com/swagger/public-api-2/swagger.json
- **API base URL:** `https://api.indyforms.com`

## Authentication

### Personal Access Token

Connect to IndyForms using a personal access token for the Public API v2.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.indyforms.com/swagger/index.html?urls.primaryName=Indyforms+Public+Api+v2)

## API conventions

Responses from this API use JSON. Response data is read from `items`.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | `POST /api/public/v2/webhooks` | [docs](https://api.indyforms.com/swagger/index.html?urls.primaryName=Indyforms+Public+Api+v2) |
| [Get Form](actions/get-form.md) | `GET /api/public/v2/forms/:id` | [docs](https://api.indyforms.com/swagger/index.html?urls.primaryName=Indyforms+Public+Api+v2) |
| [Get Record](actions/get-record.md) | `GET /api/public/v2/forms/:formId/records/:id` | [docs](https://api.indyforms.com/swagger/index.html?urls.primaryName=Indyforms+Public+Api+v2) |
| [Get User](actions/get-user.md) | `GET /api/public/v2/users/:id` | [docs](https://api.indyforms.com/swagger/index.html?urls.primaryName=Indyforms+Public+Api+v2) |
| [Get Webhook](actions/get-webhook.md) | `GET /api/public/v2/webhooks/:id` | [docs](https://api.indyforms.com/swagger/index.html?urls.primaryName=Indyforms+Public+Api+v2) |
| [List Form Records](actions/list-form-records.md) | `GET /api/public/v2/forms/:formId/records` | [docs](https://api.indyforms.com/swagger/index.html?urls.primaryName=Indyforms+Public+Api+v2) |
| [List Forms](actions/list-forms.md) | `GET /api/public/v2/forms` | [docs](https://api.indyforms.com/swagger/index.html?urls.primaryName=Indyforms+Public+Api+v2) |
| [List Users](actions/list-users.md) | `GET /api/public/v2/users` | [docs](https://api.indyforms.com/swagger/index.html?urls.primaryName=Indyforms+Public+Api+v2) |
| [List Webhooks](actions/list-webhooks.md) | `GET /api/public/v2/webhooks` | [docs](https://api.indyforms.com/swagger/index.html?urls.primaryName=Indyforms+Public+Api+v2) |
| [Update Webhook](actions/update-webhook.md) | `PUT /api/public/v2/webhooks` | [docs](https://api.indyforms.com/swagger/index.html?urls.primaryName=Indyforms+Public+Api+v2) |
