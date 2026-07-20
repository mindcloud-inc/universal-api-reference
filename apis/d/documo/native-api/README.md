# Documo: Native API Reference

A consolidated summary of Documo's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.documo.com/
- **API base URL:** `https://api.documo.com`

## Authentication

### API Key

Connect with a Documo API key generated from the Documo app.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.documo.com/hc/en-us/articles/7789630698011-How-to-Create-API-Keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `rows`.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Custom Field](actions/archive-custom-field.md) | `PATCH /v1/custom-fields/:customFieldId` | [docs](https://docs.documo.com/) |
| [Create API Key](actions/create-api-key.md) | `POST /api-keys` | [docs](https://docs.documo.com/) |
| [Create Contact](actions/create-contact.md) | `POST /v1/contacts` | [docs](https://docs.documo.com/) |
| [Create Custom Field](actions/create-custom-field.md) | `POST /v1/custom-fields` | [docs](https://docs.documo.com/) |
| [Create Folder](actions/create-folder.md) | `POST /folders` | [docs](https://docs.documo.com/) |
| [Create Tag](actions/create-tag.md) | `POST /v1/tag` | [docs](https://docs.documo.com/) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://docs.documo.com/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /v1/contacts/:contactId` | [docs](https://docs.documo.com/) |
| [Delete Custom Field](actions/delete-custom-field.md) | `DELETE /v1/custom-fields/:customFieldId` | [docs](https://docs.documo.com/) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /v1/tag/:tagId` | [docs](https://docs.documo.com/) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:webhookId` | [docs](https://docs.documo.com/) |
| [Get Current User](actions/get-current-user.md) | `GET /v1/me` | [docs](https://docs.documo.com/) |
| [Get Folder Info](actions/get-folder-info.md) | `GET /folders/:folderId/info` | [docs](https://docs.documo.com/) |
| [List API Keys](actions/list-api-keys.md) | `GET /api-keys` | [docs](https://docs.documo.com/) |
| [List Contacts](actions/list-contacts.md) | `GET /v1/contacts` | [docs](https://docs.documo.com/) |
| [List Cover Pages](actions/list-cover-pages.md) | `GET /coverpages` | [docs](https://docs.documo.com/) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /v1/custom-fields` | [docs](https://docs.documo.com/) |
| [List Tags](actions/list-tags.md) | `GET /v1/tags` | [docs](https://docs.documo.com/) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://docs.documo.com/) |
| [Send Fax](actions/send-fax.md) | `POST /v1/faxes` | [docs](https://docs.documo.com/) |
| [Update Contact](actions/update-contact.md) | `PATCH /v1/contacts/:contactId` | [docs](https://docs.documo.com/) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /webhooks/:webhookId` | [docs](https://docs.documo.com/) |
| [Upload File](actions/upload-file.md) | `POST /files` | [docs](https://docs.documo.com/) |
| [Validate Fax Number](actions/validate-fax-number.md) | `GET /v1/numbers/validate` | [docs](https://docs.documo.com/) |
