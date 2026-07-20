# Resend: Native API Reference

A consolidated summary of Resend's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://resend.com/docs/api-reference
- **OpenAPI specification:** https://raw.githubusercontent.com/resend/resend-openapi/main/resend.yaml
- **API base URL:** `https://api.resend.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://resend.com/docs/api-reference/introduction)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–100). Use `after` in the query string as the pagination cursor.

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Email](actions/cancel-email.md) | `POST /emails/:id/cancel` | [docs](https://resend.com/docs/api-reference/emails/cancel-email) |
| [Create API Key](actions/create-api-key.md) | `POST /api-keys` | [docs](https://resend.com/docs/api-reference/api-keys/create-api-key) |
| [Create Audience](actions/create-audience.md) | `POST /audiences` | [docs](https://resend.com/docs/api-reference/audiences/create-audience) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://resend.com/docs/api-reference/contacts/create-contact) |
| [Create Domain](actions/create-domain.md) | `POST /domains` | [docs](https://resend.com/docs/api-reference/domains/create-domain) |
| [Create Template](actions/create-template.md) | `POST /templates` | [docs](https://resend.com/docs/api-reference/templates/create-template) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://resend.com/docs/api-reference/webhooks/create-webhook) |
| [Delete API Key](actions/delete-api-key.md) | `DELETE /api-keys/:api_key_id` | [docs](https://resend.com/docs/api-reference/api-keys/delete-api-key) |
| [Delete Audience](actions/delete-audience.md) | `DELETE /audiences/:audience_id` | [docs](https://resend.com/docs/api-reference/audiences/delete-audience) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:id` | [docs](https://resend.com/docs/api-reference/contacts/delete-contact) |
| [Delete Domain](actions/delete-domain.md) | `DELETE /domains/:id` | [docs](https://resend.com/docs/api-reference/domains/delete-domain) |
| [Delete Template](actions/delete-template.md) | `DELETE /templates/:id` | [docs](https://resend.com/docs/api-reference/templates/delete-template) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:id` | [docs](https://resend.com/docs/api-reference/webhooks/delete-webhook) |
| [Get Template](actions/get-template.md) | `GET /templates/:id` | [docs](https://resend.com/docs/api-reference/templates/get-template) |
| [List API Keys](actions/list-api-keys.md) | `GET /api-keys` | [docs](https://resend.com/docs/api-reference/api-keys/list-api-keys) |
| [List Audiences](actions/list-audiences.md) | `GET /audiences` | [docs](https://resend.com/docs/api-reference/audiences/list-audiences) |
| [List Broadcasts](actions/list-broadcasts.md) | `GET /broadcasts` | [docs](https://resend.com/docs/api-reference/broadcasts/list-broadcasts) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://resend.com/docs/api-reference/contacts/list-contacts) |
| [List Domains](actions/list-domains.md) | `GET /domains` | [docs](https://resend.com/docs/api-reference/domains/list-domains) |
| [List Received Emails](actions/list-received-emails.md) | `GET /emails/receiving` | [docs](https://resend.com/docs/api-reference/emails/list-received-emails) |
| [List Sent Emails](actions/list-sent-emails.md) | `GET /emails` | [docs](https://resend.com/docs/api-reference/emails/list-emails) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://resend.com/docs/api-reference/templates/list-templates) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://resend.com/docs/api-reference/webhooks/list-webhooks) |
| [Retrieve Audience](actions/retrieve-audience.md) | `GET /audiences/:id` | [docs](https://resend.com/docs/api-reference/audiences/get-audience) |
| [Retrieve Contact](actions/retrieve-contact.md) | `GET /contacts/:id` | [docs](https://resend.com/docs/api-reference/contacts/get-contact) |
| [Retrieve Domain](actions/retrieve-domain.md) | `GET /domains/:id` | [docs](https://resend.com/docs/api-reference/domains/get-domain) |
| [Retrieve Email](actions/retrieve-email.md) | `GET /emails/:id` | [docs](https://resend.com/docs/api-reference/emails/retrieve-email) |
| [Retrieve Webhook](actions/retrieve-webhook.md) | `GET /webhooks/:id` | [docs](https://resend.com/docs/api-reference/webhooks/get-webhook) |
| [Send Batch Emails](actions/send-batch-emails.md) | `POST /emails/batch` | [docs](https://resend.com/docs/api-reference/emails/send-batch-emails) |
| [Send Email](actions/send-email.md) | `POST /emails` | [docs](https://resend.com/docs/api-reference/emails/send-email) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/:id` | [docs](https://resend.com/docs/api-reference/contacts/update-contact) |
| [Update Domain](actions/update-domain.md) | `PATCH /domains/:id` | [docs](https://resend.com/docs/api-reference/domains/update-domain) |
| [Update Email](actions/update-email.md) | `PATCH /emails/:id` | [docs](https://resend.com/docs/api-reference/emails/update-email) |
| [Update Template](actions/update-template.md) | `PATCH /templates/:id` | [docs](https://resend.com/docs/api-reference/templates/update-template) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /webhooks/:id` | [docs](https://resend.com/docs/api-reference/webhooks/update-webhook) |
| [Verify Domain](actions/verify-domain.md) | `POST /domains/:id/verify` | [docs](https://resend.com/docs/api-reference/domains/verify-domain) |
