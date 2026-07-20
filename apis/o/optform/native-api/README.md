# Optform: Native API Reference

A consolidated summary of Optform's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://optform.com/help/api/api
- **OpenAPI specification:** https://optform.com/swagger/api.yaml
- **API base URL:** `https://optform.azure-api.net`

## Authentication

### API Key

Provide the Optform subscription key in the Ocp-Apim-Subscription-Key header. Verified against Optform data endpoints.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Ocp-Apim-Subscription-Key: <apiKey>
```

[Official authentication documentation](https://optform.com/help/api/api)

## API conventions

Responses from this API use JSON.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Long Text Question](actions/add-long-text-question.md) | `POST /api/Form/questions` | [docs](https://optform.com/help/api/api) |
| [Create Form](actions/create-form.md) | `POST /api/Form` | [docs](https://optform.com/help/api/api) |
| [Delete Form](actions/delete-form.md) | `DELETE /api/Form/:id` | [docs](https://optform.com/help/api/api) |
| [Get Form](actions/get-form.md) | `GET /api/Form/:id` | [docs](https://optform.com/help/api/api) |
| [Get Form Questions](actions/get-form-questions.md) | `GET /api/Form/questions/all/:formId` | [docs](https://optform.com/help/api/api) |
| [List Contacts](actions/list-contacts.md) | `GET /data/api/contact` | [docs](https://optform.com/help/api/api) |
| [List Form Responses](actions/list-form-responses.md) | `GET /data/api/formResponses` | [docs](https://optform.com/help/api/api) |
| [List Lead Scores](actions/list-lead-scores.md) | `GET /data/api/score` | [docs](https://optform.com/help/api/api) |
| [List User Forms](actions/list-user-forms.md) | `GET /api/Form/user/:userId` | [docs](https://optform.com/help/api/api) |
| [List Workspace Forms](actions/list-workspace-forms.md) | `GET /api/Form/all/:workspaceId` | [docs](https://optform.com/help/api/api) |
| [Remove Question](actions/remove-question.md) | `DELETE /api/Form/:formId/questions/:questionId` | [docs](https://optform.com/help/api/api) |
| [Update Form](actions/update-form.md) | `PUT /api/Form` | [docs](https://optform.com/help/api/api) |
| [Update Long Text Question](actions/update-long-text-question.md) | `PUT /api/Form/questions` | [docs](https://optform.com/help/api/api) |
