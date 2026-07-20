# Weavely: Native API Reference

A consolidated summary of Weavely's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://help.weavely.ai/
- **API base URL:** `https://api.weavely.ai/v1`

## Authentication

### Personal Token

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.weavely.ai/integrations/personal-tokens)

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | `POST /forms` | [docs](https://help.weavely.ai/developers/forms) |
| [Create Webhook](actions/create-webhook.md) | `POST /forms/:formId/webhooks` | [docs](https://help.weavely.ai/developers/webhooks) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /forms/:formId/webhooks/:webhookId` | [docs](https://help.weavely.ai/developers/webhooks) |
| [Generate Form](actions/generate-form.md) | `POST /forms/generate` | [docs](https://help.weavely.ai/developers/forms) |
| [Get Form Fields](actions/get-form-fields.md) | `GET /forms/:formId/fields` | [docs](https://help.weavely.ai/developers/forms) |
| [Get Published Form Specification](actions/get-published-form-specification.md) | `GET https://api.weavely.ai/forms/:id/client` | [docs](https://help.weavely.ai/developers/forms) |
| [List Team Forms](actions/list-team-forms.md) | `GET /teams/:teamId/forms` | [docs](https://help.weavely.ai/developers/identity) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://help.weavely.ai/developers/identity) |
| [Update Form](actions/update-form.md) | `POST /forms/:id` | [docs](https://help.weavely.ai/developers/forms) |
