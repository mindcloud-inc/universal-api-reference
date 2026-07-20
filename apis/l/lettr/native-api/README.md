# Lettr: Native API Reference

A consolidated summary of Lettr's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://docs.lettr.com/api-reference/introduction
- **API base URL:** `https://app.lettr.com/api/`

## Authentication

### API Key

Authenticate Lettr API requests with a live API key sent as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.lettr.com/api-reference/introduction)

## API conventions

The total page count is read from `pagination.last_page`. The current page number is read from `pagination.current_page`.

## Pagination

Use `per_page` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Auth Check](actions/auth-check.md) | `GET /auth/check` | [docs](https://docs.lettr.com/api-reference/system/auth-check) |
| [Cancel Scheduled Email](actions/cancel-scheduled-email.md) | `DELETE /emails/scheduled/:transmissionId` | [docs](https://docs.lettr.com/api-reference/emails/cancel-scheduled-email) |
| [Create Domain](actions/create-domain.md) | `POST /domains` | [docs](https://docs.lettr.com/api-reference/domains/create-domain) |
| [Create Template](actions/create-template.md) | `POST /templates` | [docs](https://docs.lettr.com/api-reference/templates/create-template) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://docs.lettr.com/api-reference/webhooks/create-webhook) |
| [Delete Domain](actions/delete-domain.md) | `DELETE /domains/:domain` | [docs](https://docs.lettr.com/api-reference/domains/delete-domain) |
| [Delete Template](actions/delete-template.md) | `DELETE /templates/:slug` | [docs](https://docs.lettr.com/api-reference/templates/delete-template) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:webhookId` | [docs](https://docs.lettr.com/api-reference/webhooks/delete-webhook) |
| [Get Domain](actions/get-domain.md) | `GET /domains/:domain` | [docs](https://docs.lettr.com/api-reference/domains/get-domain) |
| [Get Email Detail](actions/get-email-detail.md) | `GET /emails/:requestId` | [docs](https://docs.lettr.com/api-reference/emails/get-email-detail) |
| [Get Scheduled Email](actions/get-scheduled-email.md) | `GET /emails/scheduled/:transmissionId` | [docs](https://docs.lettr.com/api-reference/emails/get-scheduled-email) |
| [Get Template](actions/get-template.md) | `GET /templates/:slug` | [docs](https://docs.lettr.com/api-reference/templates/get-template) |
| [Get Template Merge Tags](actions/get-template-merge-tags.md) | `GET /templates/:slug/merge-tags` | [docs](https://docs.lettr.com/api-reference/templates/get-merge-tags) |
| [Get Template Merge Tags By Version](actions/get-template-merge-tags-by-version.md) | `GET /templates/:slug/merge-tags` | [docs](https://docs.lettr.com/api-reference/templates/get-merge-tags) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/:webhookId` | [docs](https://docs.lettr.com/api-reference/webhooks/get-webhook) |
| [Health Check](actions/health-check.md) | `GET /health` | [docs](https://docs.lettr.com/api-reference/system/health-check) |
| [List Bounce Events](actions/list-bounce-events.md) | `GET /emails/events` | [docs](https://docs.lettr.com/api-reference/emails/list-email-events) |
| [List Delivery Events](actions/list-delivery-events.md) | `GET /emails/events` | [docs](https://docs.lettr.com/api-reference/emails/list-email-events) |
| [List Domains](actions/list-domains.md) | `GET /domains` | [docs](https://docs.lettr.com/api-reference/domains/list-domains) |
| [List Email Events](actions/list-email-events.md) | `GET /emails/events` | [docs](https://docs.lettr.com/api-reference/emails/list-email-events) |
| [List Email Events For Transmission](actions/list-email-events-for-transmission.md) | `GET /emails/events` | [docs](https://docs.lettr.com/api-reference/emails/list-email-events) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://docs.lettr.com/api-reference/templates/list-templates) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://docs.lettr.com/api-reference/webhooks/list-webhooks) |
| [Schedule Email](actions/schedule-email.md) | `POST /emails/scheduled` | [docs](https://docs.lettr.com/api-reference/emails/schedule-email) |
| [Schedule HTML Email](actions/schedule-html-email.md) | `POST /emails/scheduled` | [docs](https://docs.lettr.com/api-reference/emails/schedule-email) |
| [Schedule Template Email](actions/schedule-template-email.md) | `POST /emails/scheduled` | [docs](https://docs.lettr.com/api-reference/emails/schedule-email) |
| [Send Email](actions/send-email.md) | `POST /emails` | [docs](https://docs.lettr.com/api-reference/emails/send-email) |
| [Send HTML Email](actions/send-html-email.md) | `POST /emails` | [docs](https://docs.lettr.com/api-reference/emails/send-email) |
| [Send Template Email](actions/send-template-email.md) | `POST /emails` | [docs](https://docs.lettr.com/api-reference/emails/send-email) |
| [Update Template](actions/update-template.md) | `PUT /templates/:slug` | [docs](https://docs.lettr.com/api-reference/templates/update-template) |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhooks/:webhookId` | [docs](https://docs.lettr.com/api-reference/webhooks/update-webhook) |
| [Verify Domain](actions/verify-domain.md) | `POST /domains/:domain/verify` | [docs](https://docs.lettr.com/api-reference/domains/verify-domain) |
