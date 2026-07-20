# CueGrowth: Native API Reference

A consolidated summary of CueGrowth's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://cuegrowth.ai/docs/
- **OpenAPI specification:** https://api.cuegrowth.ai/public/openapi.json/
- **API base URL:** `https://api.cuegrowth.ai/public/api`

## Authentication

### API Key

Use your CueGrowth API key. MindCloud sends it as Authorization: Bearer {API_KEY} as documented by CueGrowth.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://web.cuegrowth.ai/integrations)

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Receiver To Campaign](actions/add-receiver-to-campaign.md) | `POST /actions/add_receiver_to_campaign` | [docs](https://cuegrowth.ai/docs/) |
| [Bulk Add Receivers To Campaign](actions/bulk-add-receivers-to-campaign.md) | `POST /actions/bulk/add_receiver_to_campaign` | [docs](https://cuegrowth.ai/docs/) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks/create` | [docs](https://cuegrowth.ai/webhooks/) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /webhooks/{webhook_id}/delete` | [docs](https://cuegrowth.ai/webhooks/) |
| [Get Campaign By Id](actions/get-campaign-by-id.md) | `GET /campaigns/{campaign_id}` | [docs](https://cuegrowth.ai/docs/) |
| [Get Inbox](actions/get-inbox.md) | `GET /inbox/{inbox_id}` | [docs](https://cuegrowth.ai/docs/) |
| [Get Task Status](actions/get-task-status.md) | `GET /tasks/{id}/status` | [docs](https://cuegrowth.ai/docs/) |
| [Get Webhook](actions/get-webhook.md) | `GET /webhooks/{webhook_id}` | [docs](https://cuegrowth.ai/webhooks/) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://cuegrowth.ai/docs/) |
| [List Campaigns by Receiver](actions/list-campaigns-by-receiver.md) | `GET /campaigns/get_all_by_receiver/{receiver_id}` | [docs](https://cuegrowth.ai/docs/) |
| [List Connections](actions/list-connections.md) | `GET /connections` | [docs](https://cuegrowth.ai/docs/) |
| [List Inboxes](actions/list-inboxes.md) | `GET /inbox` | [docs](https://cuegrowth.ai/docs/) |
| [List Messages](actions/list-messages.md) | `GET /messages` | [docs](https://cuegrowth.ai/docs/) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://cuegrowth.ai/docs/) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://cuegrowth.ai/webhooks/) |
| [Remove Receiver From Campaign](actions/remove-receiver-from-campaign.md) | `POST /actions/remove_receiver_from_campaign` | [docs](https://cuegrowth.ai/docs/) |
| [Retrieve Receiver](actions/retrieve-receiver.md) | `GET /receivers/retrieve` | [docs](https://cuegrowth.ai/docs/) |
| [Retrieve User](actions/retrieve-user.md) | `GET /users/retrieve` | [docs](https://cuegrowth.ai/docs/) |
| [Send Message To Inbox](actions/send-message-to-inbox.md) | `POST /inbox/{inbox_id}/send` | [docs](https://cuegrowth.ai/docs/) |
| [Send Message To Receiver](actions/send-message-to-receiver.md) | `POST /actions/send_message_to_receiver` | [docs](https://cuegrowth.ai/docs/) |
| [Update Campaign](actions/update-campaign.md) | `PUT /campaigns/{campaign_id}/update` | [docs](https://cuegrowth.ai/docs/) |
| [Update Webhook](actions/update-webhook.md) | `PUT /webhooks/{webhook_id}/update` | [docs](https://cuegrowth.ai/webhooks/) |
