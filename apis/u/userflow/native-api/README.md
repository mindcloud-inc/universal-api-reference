# Userflow: Native API Reference

A consolidated summary of Userflow's API configuration and 17 documented operations, with links to official documentation.

- **Official docs:** https://docs.userflow.com/docs/api
- **API base URL:** `https://api.userflow.com`

## Authentication

### API Key

Use a Userflow environment API key for the Users API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.userflow.com/docs/api)

## Endpoints (17 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Or Update Group](actions/create-or-update-group.md) | `POST /groups` | [docs](https://docs.userflow.com/docs/api) |
| [Create Or Update User](actions/create-or-update-user.md) | `POST /users` | [docs](https://docs.userflow.com/docs/api) |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | `POST /webhook_subscriptions` | [docs](https://docs.userflow.com/docs/api) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/:group_id` | [docs](https://docs.userflow.com/docs/api) |
| [Delete User](actions/delete-user.md) | `DELETE /users/:user_id` | [docs](https://docs.userflow.com/docs/api) |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | `DELETE /webhook_subscriptions/:webhook_subscription_id` | [docs](https://docs.userflow.com/docs/api) |
| [Get Content](actions/get-content.md) | `GET /content/:content_id` | [docs](https://docs.userflow.com/docs/api) |
| [Get User](actions/get-user.md) | `GET /users/:user_id` | [docs](https://docs.userflow.com/docs/api) |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | `GET /webhook_subscriptions/:webhook_subscription_id` | [docs](https://docs.userflow.com/docs/api) |
| [List Attribute Definitions](actions/list-attribute-definitions.md) | `GET /attribute_definitions` | [docs](https://docs.userflow.com/docs/api) |
| [List Content](actions/list-content.md) | `GET /content` | [docs](https://docs.userflow.com/docs/api) |
| [List Event Definitions](actions/list-event-definitions.md) | `GET /event_definitions` | [docs](https://docs.userflow.com/docs/api) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://docs.userflow.com/docs/api) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://docs.userflow.com/docs/api) |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | `GET /webhook_subscriptions` | [docs](https://docs.userflow.com/docs/api) |
| [Track Event](actions/track-event.md) | `POST /events` | [docs](https://docs.userflow.com/docs/api) |
| [Update Webhook Subscription](actions/update-webhook-subscription.md) | `PATCH /webhook_subscriptions/:webhook_subscription_id` | [docs](https://docs.userflow.com/docs/api) |
