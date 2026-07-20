# Sozuri (Kenya) SMS: Native API Reference

A consolidated summary of Sozuri (Kenya) SMS's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://sozuri.net/docs
- **API base URL:** `https://sozuri.net/api/v1`

## Authentication

### API Key

Authenticate with your Sozuri project name and project API key.

### Credentials

- **API Key:** `apiKey` · required
- **Project Name:** `project` · required · The Sozuri project name that owns this API key.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://sozuri.net/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. The total page count is read from `contacts.last_page`. The current page number is read from `contacts.current_page`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Contacts](actions/create-contacts.md) | `POST /contacts` | [docs](https://sozuri.net/docs/contacts) |
| [Create Subscriber](actions/create-subscriber.md) | `POST /premium` | [docs](https://sozuri.net/docs/subscription) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:contactIdOrMobile` | [docs](https://sozuri.net/docs/contacts) |
| [Delete Subscriber](actions/delete-subscriber.md) | `POST /premium` | [docs](https://sozuri.net/docs/subscription) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:contactIdOrMobile` | [docs](https://sozuri.net/docs/contacts) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://sozuri.net/docs/contacts) |
| [Send Bulk SMS](actions/send-bulk-sms.md) | `POST /messaging` | [docs](https://sozuri.net/docs/text) |
| [Send Premium Ondemand SMS](actions/send-premium-ondemand-sms.md) | `POST /premium` | [docs](https://sozuri.net/docs/ondemand) |
| [Send Premium Subscription SMS](actions/send-premium-subscription-sms.md) | `POST /premium` | [docs](https://sozuri.net/docs/subscription) |
| [Send WhatsApp Audio Message](actions/send-whats-app-audio-message.md) | `POST /messaging` | [docs](https://sozuri.net/docs/whatsapp) |
| [Send WhatsApp Contacts Message](actions/send-whats-app-contacts-message.md) | `POST /messaging` | [docs](https://sozuri.net/docs/whatsapp) |
| [Send WhatsApp Document Message](actions/send-whats-app-document-message.md) | `POST /messaging` | [docs](https://sozuri.net/docs/whatsapp) |
| [Send WhatsApp Image Message](actions/send-whats-app-image-message.md) | `POST /messaging` | [docs](https://sozuri.net/docs/whatsapp) |
| [Send WhatsApp Interactive List Message](actions/send-whats-app-interactive-list-message.md) | `POST /messaging` | [docs](https://sozuri.net/docs/whatsapp) |
| [Send WhatsApp Interactive Reply Buttons Message](actions/send-whats-app-interactive-reply-buttons-message.md) | `POST /messaging` | [docs](https://sozuri.net/docs/whatsapp) |
| [Send WhatsApp Location Message](actions/send-whats-app-location-message.md) | `POST /messaging` | [docs](https://sozuri.net/docs/whatsapp) |
| [Send WhatsApp Reaction Message](actions/send-whats-app-reaction-message.md) | `POST /messaging` | [docs](https://sozuri.net/docs/whatsapp) |
| [Send WhatsApp Reply Text Message](actions/send-whats-app-reply-text-message.md) | `POST /messaging` | [docs](https://sozuri.net/docs/whatsapp) |
| [Send WhatsApp Sticker Message](actions/send-whats-app-sticker-message.md) | `POST /messaging` | [docs](https://sozuri.net/docs/whatsapp) |
| [Send WhatsApp Text Message](actions/send-whats-app-text-message.md) | `POST /messaging` | [docs](https://sozuri.net/docs/whatsapp) |
| [Send WhatsApp Video Message](actions/send-whats-app-video-message.md) | `POST /messaging` | [docs](https://sozuri.net/docs/whatsapp) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:contactIdOrMobile` | [docs](https://sozuri.net/docs/contacts) |
