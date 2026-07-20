# ActivitySmith: Native API Reference

A consolidated summary of ActivitySmith's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://activitysmith.com/docs
- **API base URL:** `https://activitysmith.com/api`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://activitysmith.com/docs/api-keys)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [End Live Activity](actions/end-live-activity.md) | `POST /live-activity/end` | [docs](https://activitysmith.com/docs/api-reference/endpoint/live-activity-end) |
| [Send Push Notification](actions/send-push-notification.md) | `POST /push-notification` | [docs](https://activitysmith.com/docs/api-reference/endpoint/push-notification) |
| [Start Live Activity](actions/start-live-activity.md) | `POST /live-activity/start` | [docs](https://activitysmith.com/docs/api-reference/endpoint/live-activity-start) |
| [Update Live Activity](actions/update-live-activity.md) | `POST /live-activity/update` | [docs](https://activitysmith.com/docs/api-reference/endpoint/live-activity-update) |
