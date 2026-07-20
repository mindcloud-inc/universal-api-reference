# Sendcrux: Native API Reference

A consolidated summary of Sendcrux's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://api.sendbound.com/
- **API base URL:** `https://sendcrux.com`

## Authentication

### API Key

Use your Sendcrux API token to authorize REST API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://sendcrux.com/frontend/docs/api/v1)

## Pagination

Use `per_page` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Email List Field](actions/add-email-list-field.md) | `POST /api/v1/lists/:uid/add-field` | [docs](https://api.sendbound.com/email-list/) |
| [Add Subscriber Tags](actions/add-subscriber-tags.md) | `POST /api/v1/subscribers/:uid/add-tag` | [docs](https://api.sendbound.com/subscribers/) |
| [Create Email List](actions/create-email-list.md) | `POST /api/v1/lists` | [docs](https://api.sendbound.com/email-list/) |
| [Create Subscriber](actions/create-subscriber.md) | `POST /api/v1/subscribers` | [docs](https://api.sendbound.com/subscribers/) |
| [Delete Email List](actions/delete-email-list.md) | `DELETE /api/v1/lists` | [docs](https://api.sendbound.com/email-list/) |
| [Delete Subscriber](actions/delete-subscriber.md) | `DELETE /api/v1/subscribers/:uid` | [docs](https://api.sendbound.com/subscribers/) |
| [Find Subscribers By Email](actions/find-subscribers-by-email.md) | `GET /api/v1/subscribers/email/:email` | [docs](https://api.sendbound.com/subscribers/) |
| [Generate Login Token](actions/generate-login-token.md) | `POST /api/v1/login-token` | [docs](https://api.sendbound.com/authentication/) |
| [Get Campaign](actions/get-campaign.md) | `GET /api/v1/campaigns/:uid` | [docs](https://api.sendbound.com/campaign/) |
| [Get Email List](actions/get-email-list.md) | `GET /api/v1/lists/:uid` | [docs](https://api.sendbound.com/email-list/) |
| [Get Subscriber](actions/get-subscriber.md) | `GET /api/v1/subscribers/:uid` | [docs](https://api.sendbound.com/subscribers/) |
| [List Active Campaigns](actions/list-active-campaigns.md) | `GET /api/v1/campaigns` | [docs](https://api.sendbound.com/campaign/) |
| [List Campaigns](actions/list-campaigns.md) | `GET /api/v1/campaigns` | [docs](https://api.sendbound.com/campaign/) |
| [List Email Lists](actions/list-email-lists.md) | `GET /api/v1/lists` | [docs](https://api.sendbound.com/email-list/) |
| [List Subscribed Subscribers](actions/list-subscribed-subscribers.md) | `GET /api/v1/subscribers` | [docs](https://api.sendbound.com/subscribers/) |
| [List Subscribers](actions/list-subscribers.md) | `GET /api/v1/subscribers` | [docs](https://api.sendbound.com/subscribers/) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /api/v1/subscriptions` |  |
| [List Subscriptions By Plan](actions/list-subscriptions-by-plan.md) | `GET /api/v1/subscriptions` |  |
| [Pause Campaign](actions/pause-campaign.md) | `POST /api/v1/campaigns/:uid/pause` | [docs](https://api.sendbound.com/campaign/) |
| [Send Abuse Notification](actions/send-abuse-notification.md) | `POST /api/v1/notification` | [docs](https://api.sendbound.com/notification/) |
| [Send Bounce Notification](actions/send-bounce-notification.md) | `POST /api/v1/notification` | [docs](https://api.sendbound.com/notification/) |
| [Send Delivery Notification](actions/send-delivery-notification.md) | `POST /api/v1/notification` | [docs](https://api.sendbound.com/notification/) |
| [Send Failed Notification](actions/send-failed-notification.md) | `POST /api/v1/notification` | [docs](https://api.sendbound.com/notification/) |
| [Send Notification](actions/send-notification.md) | `POST /api/v1/notification` | [docs](https://api.sendbound.com/notification/) |
| [Send Spam Notification](actions/send-spam-notification.md) | `POST /api/v1/notification` | [docs](https://api.sendbound.com/notification/) |
| [Subscribe Subscriber to List](actions/subscribe-subscriber-to-list.md) | `PATCH /api/v1/lists/:list_uid/subscribers/:uid/subscribe` | [docs](https://api.sendbound.com/subscribers/) |
| [Unsubscribe Subscriber from List](actions/unsubscribe-subscriber-from-list.md) | `PATCH /api/v1/lists/:list_uid/subscribers/:uid/unsubscribe` | [docs](https://api.sendbound.com/subscribers/) |
| [Update Subscriber](actions/update-subscriber.md) | `PATCH /api/v1/subscribers/:uid` | [docs](https://api.sendbound.com/subscribers/) |
| [Upload Files](actions/upload-files.md) | `POST /api/v1/file/upload` | [docs](https://api.sendbound.com/files/) |
