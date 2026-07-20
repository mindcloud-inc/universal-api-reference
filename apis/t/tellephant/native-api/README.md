# Tellephant: Native API Reference

A consolidated summary of Tellephant's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://app.tellephant.com/api-documentation
- **API base URL:** `https://api.tellephant.com`

## Authentication

### API Key

Authenticate Tellephant API requests with an API key sent as the `apikey` JSON body field.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.tellephant.com/api-documentation)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create tags](actions/create-tags.md) | `PUT /v1/user/tags/create` | [docs](https://app.tellephant.com/api-documentation#create-tags-on-platform) |
| [Get contact tags](actions/get-contact-tags.md) | `POST /v1/user/contacts/:contactId/tags` | [docs](https://app.tellephant.com/api-documentation#fetch-contact-info) |
| [Get message history](actions/get-message-history.md) | `POST /v1/message-history` | [docs](https://app.tellephant.com/api-documentation#message-history) |
| [Get webhooks](actions/get-webhooks.md) | `POST https://app.tellephant.com/api/v2/user/webhook` | [docs](https://app.tellephant.com/api-documentation#get-webhooks) |
| [List incoming logs](actions/list-incoming-logs.md) | `POST /v1/user/logs` | [docs](https://app.tellephant.com/api-documentation#get-incoming-logs) |
| [List outgoing logs](actions/list-outgoing-logs.md) | `POST /v1/user/logs` | [docs](https://app.tellephant.com/api-documentation#get-outgoing-logs) |
| [List template logs](actions/list-template-logs.md) | `POST /v1/user/logs` | [docs](https://app.tellephant.com/api-documentation#get-template-logs) |
| [List unsubscribed contacts](actions/list-unsubscribed-contacts.md) | `POST /v1/user/unsubscribe` | [docs](https://app.tellephant.com/api-documentation#get-contact) |
| [Send OTP](actions/send-otp.md) | `POST /v1/send-otp` | [docs](https://app.tellephant.com/api-documentation#otp-service) |
| [Send WhatsApp session message](actions/send-whats-app-session-message.md) | `POST /v1/send-message` | [docs](https://app.tellephant.com/api-documentation#session-messages) |
| [Send WhatsApp template message](actions/send-whats-app-template-message.md) | `POST /v1/send-message` | [docs](https://app.tellephant.com/api-documentation#template-messages) |
| [Update contact tags](actions/update-contact-tags.md) | `PATCH /v1/user/tags/update` | [docs](https://app.tellephant.com/api-documentation#update-tags-for-contacts) |
| [Update unsubscribe status](actions/update-unsubscribe-status.md) | `POST /v1/user/unsubscribe/update` | [docs](https://app.tellephant.com/api-documentation#update-contact) |
| [Update webhook](actions/update-webhook.md) | `POST https://app.tellephant.com/api/v2/user/webhook/update` | [docs](https://app.tellephant.com/api-documentation#update-webhooks) |
| [Validate OTP](actions/validate-otp.md) | `POST /v1/validate-otp` | [docs](https://app.tellephant.com/api-documentation#otp-service) |
