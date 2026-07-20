# WhatsBox: Native API Reference

A consolidated summary of WhatsBox's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://api.whatsbox.io/docs
- **OpenAPI specification:** https://api.whatsbox.io/docs/json
- **API base URL:** `https://api.whatsbox.io`

## Authentication

### API Key

Connect with a WhatsBox API key generated from Settings -> API Keys.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://api.whatsbox.io/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Service Health](actions/check-service-health.md) | `GET /` | [docs](https://api.whatsbox.io/docs) |
| [Create Contact List](actions/create-contact-list.md) | `POST /contact-lists` | [docs](https://api.whatsbox.io/docs) |
| [Delete Contact List](actions/delete-contact-list.md) | `DELETE /contact-lists/:id` | [docs](https://api.whatsbox.io/docs) |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | `DELETE /webhook-subscriptions/:id` | [docs](https://api.whatsbox.io/docs) |
| [Get Contact List](actions/get-contact-list.md) | `GET /contact-lists/:id` | [docs](https://api.whatsbox.io/docs) |
| [Get My Organization](actions/get-my-organization.md) | `GET /orgs/my` | [docs](https://api.whatsbox.io/docs) |
| [Get Template](actions/get-template.md) | `GET /templates/:id` | [docs](https://api.whatsbox.io/docs) |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | `GET /webhook-subscriptions/:id` | [docs](https://api.whatsbox.io/docs) |
| [List Channels](actions/list-channels.md) | `GET /channels` | [docs](https://api.whatsbox.io/docs#tag/channels/GET/channels) |
| [List Contact Lists](actions/list-contact-lists.md) | `GET /contact-lists` | [docs](https://api.whatsbox.io/docs#tag/messages/POST/messages/template) |
| [List Team Members](actions/list-team-members.md) | `GET /team-members` | [docs](https://api.whatsbox.io/docs#tag/team-members/GET/team-members) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://api.whatsbox.io/docs) |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | `GET /webhook-subscriptions` | [docs](https://api.whatsbox.io/docs) |
| [Send Media Message](actions/send-media-message.md) | `POST /messages/media` | [docs](https://api.whatsbox.io/docs) |
| [Send Template Message](actions/send-template-message.md) | `POST /messages/template` | [docs](https://api.whatsbox.io/docs#tag/messages/POST/messages/template) |
| [Send Text Message](actions/send-text-message.md) | `POST /messages/text` | [docs](https://api.whatsbox.io/docs) |
| [Update Contact List](actions/update-contact-list.md) | `PUT /contact-lists/:id` | [docs](https://api.whatsbox.io/docs) |
| [Upsert Webhook Subscription](actions/upsert-webhook-subscription.md) | `POST /webhook-subscriptions` | [docs](https://api.whatsbox.io/docs) |
