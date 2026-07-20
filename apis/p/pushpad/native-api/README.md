# Pushpad: Native API Reference

A consolidated summary of Pushpad's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://pushpad.xyz/docs/rest_api
- **OpenAPI specification:** https://pushpad.xyz/openapi.yaml
- **API base URL:** `https://pushpad.xyz/api/v1`

## Authentication

### API Token

Authenticate Pushpad requests with a bearer access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://pushpad.xyz/docs/rest_api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Scheduled Notification](actions/cancel-scheduled-notification.md) | `DELETE /notifications/:notification_id/cancel` | [docs](https://pushpad.xyz/docs/rest_api#notifications_api_docs) |
| [Create or Import Subscription](actions/create-or-import-subscription.md) | `POST /projects/:project_id/subscriptions` | [docs](https://pushpad.xyz/docs/rest_api#subscriptions_api_docs) |
| [Create Project](actions/create-project.md) | `POST /projects` | [docs](https://pushpad.xyz/docs/rest_api#projects_api_docs) |
| [Create Sender](actions/create-sender.md) | `POST /senders` | [docs](https://pushpad.xyz/docs/rest_api#senders_api_docs) |
| [Delete Project](actions/delete-project.md) | `DELETE /projects/:project_id` | [docs](https://pushpad.xyz/docs/rest_api#projects_api_docs) |
| [Delete Sender](actions/delete-sender.md) | `DELETE /senders/:sender_id` | [docs](https://pushpad.xyz/docs/rest_api#senders_api_docs) |
| [Delete Subscription](actions/delete-subscription.md) | `DELETE /projects/:project_id/subscriptions/:subscription_id` | [docs](https://pushpad.xyz/docs/rest_api#subscriptions_api_docs) |
| [Get Notification](actions/get-notification.md) | `GET /notifications/:notification_id` | [docs](https://pushpad.xyz/docs/rest_api#notifications_api_docs) |
| [Get Project](actions/get-project.md) | `GET /projects/:project_id` | [docs](https://pushpad.xyz/docs/rest_api#projects_api_docs) |
| [Get Sender](actions/get-sender.md) | `GET /senders/:sender_id` | [docs](https://pushpad.xyz/docs/rest_api#senders_api_docs) |
| [Get Subscription](actions/get-subscription.md) | `GET /projects/:project_id/subscriptions/:subscription_id` | [docs](https://pushpad.xyz/docs/rest_api#subscriptions_api_docs) |
| [List Latest Notifications](actions/list-latest-notifications.md) | `GET /projects/:project_id/notifications` | [docs](https://pushpad.xyz/docs/rest_api#notifications_api_docs) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://pushpad.xyz/docs/rest_api#projects_api_docs) |
| [List Senders](actions/list-senders.md) | `GET /senders` | [docs](https://pushpad.xyz/docs/rest_api#senders_api_docs) |
| [List Subscriptions](actions/list-subscriptions.md) | `GET /projects/:project_id/subscriptions` | [docs](https://pushpad.xyz/docs/rest_api#subscriptions_api_docs) |
| [Send Notification](actions/send-notification.md) | `POST /projects/:project_id/notifications` | [docs](https://pushpad.xyz/docs/rest_api#notifications_api_docs) |
| [Update Project](actions/update-project.md) | `PATCH /projects/:project_id` | [docs](https://pushpad.xyz/docs/rest_api#projects_api_docs) |
| [Update Sender](actions/update-sender.md) | `PATCH /senders/:sender_id` | [docs](https://pushpad.xyz/docs/rest_api#senders_api_docs) |
| [Update Subscription](actions/update-subscription.md) | `PATCH /projects/:project_id/subscriptions/:subscription_id` | [docs](https://pushpad.xyz/docs/rest_api#subscriptions_api_docs) |
