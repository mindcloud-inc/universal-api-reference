# Pipeless Recommendations: Native API Reference

A consolidated summary of Pipeless Recommendations's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://docs.pipeless.io/reference
- **API base URL:** `https://api.pipeless.io`

## Authentication

### API Token

Use a Pipeless app API token. MindCloud stores one token and sends it as the raw Authorization header required by the Pipeless API.

### Credentials

- **API Token:** `apiKey` · required · Paste the Pipeless app API token. MindCloud sends this value as the raw Authorization header.

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://docs.pipeless.io/docs/adding-an-app)

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Event](actions/create-event.md) | `POST /v1/apps/:appId/events` | [docs](https://docs.pipeless.io/reference/create-event) |
| [Create Events Batch](actions/create-events-batch.md) | `POST /v1/apps/:appId/events/batch` | [docs](https://docs.pipeless.io/reference/create-events-batch) |
| [Delete All Objects By Type](actions/delete-all-objects-by-type.md) | `DELETE /v1/apps/:appId/objects/all` | [docs](https://docs.pipeless.io/reference/delete-all-objects-by-type) |
| [Delete Event](actions/delete-event.md) | `DELETE /v1/apps/:appId/events` | [docs](https://docs.pipeless.io/reference/delete-event) |
| [Delete Object](actions/delete-object.md) | `DELETE /v1/apps/:appId/objects` | [docs](https://docs.pipeless.io/reference/delete-object) |
| [Edit Object](actions/edit-object.md) | `PATCH /v1/apps/:appId/objects` | [docs](https://docs.pipeless.io/reference/edit-object) |
| [Get Activity Actions Feed](actions/get-activity-actions-feed.md) | `GET /v1/apps/:appId/algos/activity/actions-feed` | [docs](https://docs.pipeless.io/reference/get-activity-actions-feed) |
| [Get Activity Feed](actions/get-activity-feed.md) | `GET /v1/apps/:appId/algos/activity/feed` | [docs](https://docs.pipeless.io/reference/get-activity-feed) |
| [Get Activity On Object](actions/get-activity-on-object.md) | `GET /v1/apps/:appId/algos/activity/object` | [docs](https://docs.pipeless.io/reference/get-activity-on-object) |
| [Get Object](actions/get-object.md) | `GET /v1/apps/:appId/objects` | [docs](https://docs.pipeless.io/reference/get-object) |
| [Get Recent Events](actions/get-recent-events.md) | `GET /v1/apps/:appId/recent-events` | [docs](https://docs.pipeless.io/reference/get-recent-events) |
| [Get Recommended Content](actions/get-recommended-content.md) | `GET /v1/apps/:appId/algos/recommendations/content` | [docs](https://docs.pipeless.io/reference/get-recommended-content) |
| [Get Recommended Users To Follow](actions/get-recommended-users-to-follow.md) | `GET /v1/apps/:appId/algos/recommendations/users-to-follow` | [docs](https://docs.pipeless.io/reference/get-recommended-users-to-follow) |
| [Get Related Content](actions/get-related-content.md) | `GET /v1/apps/:appId/algos/recommendations/related-content` | [docs](https://docs.pipeless.io/reference/get-related-content) |
| [Get Related Tags](actions/get-related-tags.md) | `GET /v1/apps/:appId/algos/recommendations/related-tags` | [docs](https://docs.pipeless.io/reference/get-related-tags) |
| [Get Related Users](actions/get-related-users.md) | `GET /v1/apps/:appId/algos/recommendations/related-users` | [docs](https://docs.pipeless.io/reference/get-related-users) |
| [Get Relationship Counts](actions/get-relationship-counts.md) | `GET /v1/apps/:appId/relationship-counts` | [docs](https://docs.pipeless.io/reference/get-relationship-counts) |
| [Get Relationship Exists](actions/get-relationship-exists.md) | `GET /v1/apps/:appId/relationship-exists` | [docs](https://docs.pipeless.io/reference/get-relationship-exists) |
| [Get Sorted Content](actions/get-sorted-content.md) | `GET /v1/apps/:appId/algos/recommendations/sorted-content` | [docs](https://docs.pipeless.io/reference/getsortedcontent) |
