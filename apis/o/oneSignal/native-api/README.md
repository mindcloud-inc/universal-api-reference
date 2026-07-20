# OneSignal: Native API Reference

A consolidated summary of OneSignal's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://documentation.onesignal.com/reference/rest-api-overview
- **API base URL:** `https://api.onesignal.com`

## Authentication

### App API Key

Connect with a OneSignal App API key.

### Credentials

- **API Key:** `apiKey` · required
- **App ID:** `appId` · required · Your OneSignal App ID in UUID v4 format.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://documentation.onesignal.com/docs/en/keys-and-ids)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create or Update Alias](actions/create-or-update-alias.md) | `PATCH /apps/:app_id/users/by/:alias_label/:alias_id/identity` | [docs](https://documentation.onesignal.com/reference/create-alias) |
| [Create Subscription by Alias](actions/create-subscription-by-alias.md) | `POST /apps/:app_id/users/by/:alias_label/:alias_id/subscriptions` | [docs](https://documentation.onesignal.com/reference/create-subscription) |
| [Create Template](actions/create-template.md) | `POST /templates` | [docs](https://documentation.onesignal.com/reference/create-template) |
| [Create User](actions/create-user.md) | `POST /apps/:app_id/users` | [docs](https://documentation.onesignal.com/reference/create-user) |
| [Delete Subscription](actions/delete-subscription.md) | `DELETE /apps/:app_id/subscriptions/:subscription_id` | [docs](https://documentation.onesignal.com/reference/delete-subscription) |
| [Delete Template](actions/delete-template.md) | `DELETE /templates/:template_id` | [docs](https://documentation.onesignal.com/reference/delete-template) |
| [Delete User](actions/delete-user.md) | `DELETE /apps/:app_id/users/by/:alias_label/:alias_id` | [docs](https://documentation.onesignal.com/reference/delete-user) |
| [Export Audience Activity CSV](actions/export-audience-activity-csv.md) | `POST /notifications/:message_id/export_events` | [docs](https://documentation.onesignal.com/reference/export-csv-of-events) |
| [Get Message](actions/get-message.md) | `GET /notifications/:notification_id` | [docs](https://documentation.onesignal.com/reference/view-message) |
| [Get Segment](actions/get-segment.md) | `GET /apps/:app_id/segments/:segment_id` | [docs](https://documentation.onesignal.com/reference/view-segment) |
| [Get Template](actions/get-template.md) | `GET /templates/:template_id` | [docs](https://documentation.onesignal.com/reference/view-template) |
| [Get User](actions/get-user.md) | `GET /apps/:app_id/users/by/:alias_label/:alias_id` | [docs](https://documentation.onesignal.com/reference/view-user) |
| [List Messages](actions/list-messages.md) | `GET /notifications` | [docs](https://documentation.onesignal.com/reference/view-messages) |
| [List Segments](actions/list-segments.md) | `GET /apps/:app_id/segments` | [docs](https://documentation.onesignal.com/reference/view-segments) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://documentation.onesignal.com/reference/view-templates) |
| [Remove Alias](actions/remove-alias.md) | `DELETE /apps/:app_id/users/by/:alias_label/:alias_id/identity/:alias_label_to_delete` | [docs](https://documentation.onesignal.com/reference/delete-alias) |
| [Update Subscription by ID](actions/update-subscription-by-id.md) | `PATCH /apps/:app_id/subscriptions/:subscription_id` | [docs](https://documentation.onesignal.com/reference/update-subscription) |
| [Update Template](actions/update-template.md) | `PATCH /templates/:template_id` | [docs](https://documentation.onesignal.com/reference/update-template) |
| [Update User](actions/update-user.md) | `PATCH /apps/:app_id/users/by/:alias_label/:alias_id` | [docs](https://documentation.onesignal.com/reference/update-user) |
