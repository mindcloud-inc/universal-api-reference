# Fliqr AI: Native API Reference

A consolidated summary of Fliqr AI's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://docs.fliqr.ai/api-reference/introduction
- **OpenAPI specification:** https://docs.fliqr.ai/api-reference/openapi.json
- **API base URL:** `https://app.fliqr.ai/api/`

## Authentication

### API Key

Authenticate Fliqr AI API requests with an X-ACCESS-TOKEN header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.fliqr.ai/api-reference/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Tag To Contact](actions/add-tag-to-contact.md) | `POST /users/:user_id/tags/:tag_id` | [docs](https://docs.fliqr.ai/api-reference/users/post-users-tags) |
| [Create Account Custom Field](actions/create-account-custom-field.md) | `POST /accounts/custom_fields` | [docs](https://docs.fliqr.ai/api-reference/accounts/post-accountscustom-fields) |
| [Create Account Tag](actions/create-account-tag.md) | `POST /accounts/tags` | [docs](https://docs.fliqr.ai/api-reference/accounts/post-accountstags) |
| [Create Contact](actions/create-contact.md) | `POST /users` | [docs](https://docs.fliqr.ai/api-reference/users/post-users) |
| [Find Account Tag By Name](actions/find-account-tag-by-name.md) | `GET /accounts/tags/name/:tag_name` | [docs](https://docs.fliqr.ai/api-reference/accounts/get-accountstagsname) |
| [Find Contacts By Custom Field](actions/find-contacts-by-custom-field.md) | `GET /users/find_by_custom_field` | [docs](https://docs.fliqr.ai/api-reference/users/get-usersfind-by-custom-field) |
| [Get Account Custom Field](actions/get-account-custom-field.md) | `GET /accounts/custom_fields/:custom_field_id` | [docs](https://docs.fliqr.ai/api-reference/accounts/get-accountscustom-fields-1) |
| [Get Account Tag](actions/get-account-tag.md) | `GET /accounts/tags/:tag_id` | [docs](https://docs.fliqr.ai/api-reference/accounts/get-accountstags-1) |
| [Get Bot Field Value](actions/get-bot-field-value.md) | `GET /accounts/bot_fields/:bot_field_id` | [docs](https://docs.fliqr.ai/api-reference/accounts/get-accountsbot-fields) |
| [Get Business Account Details](actions/get-business-account-details.md) | `GET /accounts/me` | [docs](https://docs.fliqr.ai/api-reference/accounts/get-accountsme) |
| [Get Contact](actions/get-contact.md) | `GET /users/:user_id` | [docs](https://docs.fliqr.ai/api-reference/users/get-users) |
| [List Account Admins](actions/list-account-admins.md) | `GET /accounts/admins` | [docs](https://docs.fliqr.ai/api-reference/accounts/get-accountsadmins) |
| [List Account Custom Fields](actions/list-account-custom-fields.md) | `GET /accounts/custom_fields` | [docs](https://docs.fliqr.ai/api-reference/accounts/get-accountscustom-fields) |
| [List Account Flows](actions/list-account-flows.md) | `GET /accounts/flows` | [docs](https://docs.fliqr.ai/api-reference/accounts/get-accountsflows) |
| [List Account Tags](actions/list-account-tags.md) | `GET /accounts/tags` | [docs](https://docs.fliqr.ai/api-reference/accounts/get-accountstags) |
| [List Contact Custom Fields](actions/list-contact-custom-fields.md) | `GET /users/:user_id/custom_fields` | [docs](https://docs.fliqr.ai/api-reference/users/get-users-custom-fields) |
| [List Contact Tags](actions/list-contact-tags.md) | `GET /users/:user_id/tags` | [docs](https://docs.fliqr.ai/api-reference/users/get-users-tags) |
| [List Pipelines](actions/list-pipelines.md) | `GET /pipelines/` | [docs](https://docs.fliqr.ai/api-reference/pipelines/get-pipelines) |
| [Remove Tag From Contact](actions/remove-tag-from-contact.md) | `DELETE /users/:user_id/tags/:tag_id` | [docs](https://docs.fliqr.ai/api-reference/users/delete-users-tags) |
| [Send Flow To Contact](actions/send-flow-to-contact.md) | `POST /users/:user_id/send/:flow_id` | [docs](https://docs.fliqr.ai/api-reference/users/post-users-send) |
| [Send Text Message To Contact](actions/send-text-message-to-contact.md) | `POST /users/:user_id/send/text` | [docs](https://docs.fliqr.ai/api-reference/users/post-users-sendtext) |
| [Set Bot Field Value](actions/set-bot-field-value.md) | `POST /accounts/bot_fields/:bot_field_id` | [docs](https://docs.fliqr.ai/api-reference/accounts/post-accountsbot-fields) |
| [Set Contact Custom Field](actions/set-contact-custom-field.md) | `POST /users/:user_id/custom_fields/:custom_field_id` | [docs](https://docs.fliqr.ai/api-reference/users/post-users-custom-fields) |
