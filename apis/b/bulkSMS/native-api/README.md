# BulkSMS: Native API Reference

A consolidated summary of BulkSMS's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://www.bulksms.com/developer/json/v1/
- **OpenAPI specification:** https://www.bulksms.com/developer/json/v1/openapi.yaml
- **API base URL:** `https://api.bulksms.com/v1`

## Authentication

### API Token Basic Auth

Authenticate BulkSMS JSON REST API requests with HTTP Basic Auth. Use the BulkSMS API token ID as the username and the token secret as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://www.bulksms.com/developer/json/v1/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–10000).

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Attachment Upload URL](actions/create-attachment-upload-url.md) | `POST /rmm/pre-sign-attachment` | [docs](https://www.bulksms.com/developer/json/v1/#tag/attachments/POST/rmm/pre-sign-attachment) |
| [Create Blocked Numbers](actions/create-blocked-numbers.md) | `POST /blocked-numbers` | [docs](https://www.bulksms.com/developer/json/v1/#tag/blocked-numbers/POST/blocked-numbers) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://www.bulksms.com/developer/json/v1/#tag/webhooks/POST/webhooks) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/:id` | [docs](https://www.bulksms.com/developer/json/v1/#tag/webhooks/DELETE/webhooks/{id}) |
| [Get Profile](actions/get-profile.md) | `GET /profile` | [docs](https://www.bulksms.com/developer/json/v1/#tag/profile/GET/profile) |
| [List Blocked Numbers](actions/list-blocked-numbers.md) | `GET /blocked-numbers` | [docs](https://www.bulksms.com/developer/json/v1/#tag/blocked-numbers/GET/blocked-numbers) |
| [List Related Messages](actions/list-related-messages.md) | `GET /messages/:id/relatedReceivedMessages` | [docs](https://www.bulksms.com/developer/json/v1/#tag/message/GET/messages/{id}/relatedReceivedMessages) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://www.bulksms.com/developer/json/v1/#tag/webhooks/GET/webhooks) |
| [Read Webhook](actions/read-webhook.md) | `GET /webhooks/:id` | [docs](https://www.bulksms.com/developer/json/v1/#tag/webhooks/GET/webhooks/{id}) |
| [Retrieve Messages](actions/retrieve-messages.md) | `GET /messages` | [docs](https://www.bulksms.com/developer/json/v1/#tag/message/GET/messages) |
| [Send Messages](actions/send-messages.md) | `POST /messages` | [docs](https://www.bulksms.com/developer/json/v1/#tag/message/POST/messages) |
| [Show Message](actions/show-message.md) | `GET /messages/:id` | [docs](https://www.bulksms.com/developer/json/v1/#tag/message/GET/messages/{id}) |
| [Transfer Credits](actions/transfer-credits.md) | `POST /credit/transfer` | [docs](https://www.bulksms.com/developer/json/v1/#tag/credits/POST/credit/transfer) |
| [Update Webhook](actions/update-webhook.md) | `POST /webhooks/:id` | [docs](https://www.bulksms.com/developer/json/v1/#tag/webhooks/POST/webhooks/{id}) |
