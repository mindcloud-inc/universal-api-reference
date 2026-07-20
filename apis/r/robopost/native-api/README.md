# Robopost: Native API Reference

A consolidated summary of Robopost's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://robopost.app/docs/robopost-api/
- **API base URL:** `https://public-api.robopost.app/v1`

## Authentication

### API Key

Use a Robopost API key from Team -> Manage API Keys. Robopost documents API integration for Pro and Agency plans.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://robopost.app/docs/manage-api-key/)

## Pagination

Use `limit` in the query string to set the page size (default 10). Use `skip` in the query string as the record offset.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort_order` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Video Task](actions/cancel-video-task.md) | `DELETE /video-tasks/{task_id}` | [docs](https://robopost.app/docs/robopost-api/) |
| [Create Scheduled Posts](actions/create-scheduled-posts.md) | `POST /scheduled_posts/` | [docs](https://robopost.app/docs/robopost-api/) |
| [Create Video Generation Task](actions/create-video-generation-task.md) | `POST /video-tasks/{series_id}/generate` | [docs](https://robopost.app/docs/robopost-api/) |
| [Create Video Series](actions/create-video-series.md) | `POST /video-series/` | [docs](https://robopost.app/docs/robopost-api/) |
| [Delete Video Series](actions/delete-video-series.md) | `DELETE /video-series/{series_id}` | [docs](https://robopost.app/docs/robopost-api/) |
| [Get Aggregated Analytics by ID](actions/get-aggregated-analytics-by-id.md) | `GET /aggregated_posts_analytics/{id}` | [docs](https://robopost.app/docs/robopost-api/) |
| [Get Social Inbox Item](actions/get-social-inbox-item.md) | `GET /social_inbox_items/{id}` | [docs](https://robopost.app/docs/robopost-api/) |
| [Get Unread Count](actions/get-unread-count.md) | `GET /social_inbox_items/unread/count` | [docs](https://robopost.app/docs/robopost-api/) |
| [Get Unread Count by Channel](actions/get-unread-count-by-channel.md) | `GET /social_inbox_items/unread/by_channel` | [docs](https://robopost.app/docs/robopost-api/) |
| [Get Video Series](actions/get-video-series.md) | `GET /video-series/{series_id}` | [docs](https://robopost.app/docs/robopost-api/) |
| [Get Video Task](actions/get-video-task.md) | `GET /video-tasks/{task_id}` | [docs](https://robopost.app/docs/robopost-api/) |
| [Get Video Task Details](actions/get-video-task-details.md) | `GET /video-tasks/{task_id}/details` | [docs](https://robopost.app/docs/robopost-api/) |
| [List Aggregated Analytics](actions/list-aggregated-analytics.md) | `GET /aggregated_posts_analytics/` | [docs](https://robopost.app/docs/robopost-api/) |
| [List Channels](actions/list-channels.md) | `GET /channels/` | [docs](https://robopost.app/docs/robopost-api/) |
| [List GMB Threads for One Channel](actions/list-gmb-threads-for-one-channel.md) | `GET /social_inbox_items/channels/{channel_id}/gmb/threads` | [docs](https://robopost.app/docs/robopost-api/) |
| [List Post Collections](actions/list-post-collections.md) | `GET /post_collections/` | [docs](https://robopost.app/docs/robopost-api/) |
| [List Social Inbox Items](actions/list-social-inbox-items.md) | `GET /social_inbox_items/` | [docs](https://robopost.app/docs/robopost-api/) |
| [List Social Inbox Threads Grouped by Post](actions/list-social-inbox-threads-grouped-by-post.md) | `GET /social_inbox_items/threads` | [docs](https://robopost.app/docs/robopost-api/) |
| [List Video Series](actions/list-video-series.md) | `GET /video-series/` | [docs](https://robopost.app/docs/robopost-api/) |
| [List Video Tasks](actions/list-video-tasks.md) | `GET /video-tasks/` | [docs](https://robopost.app/docs/robopost-api/) |
| [Ping](actions/ping.md) | `GET https://public-api.robopost.app/ping` | [docs](https://robopost.app/docs/robopost-api/) |
| [Update Video Series](actions/update-video-series.md) | `PUT /video-series/{series_id}` | [docs](https://robopost.app/docs/robopost-api/) |
| [Upload Media](actions/upload-media.md) | `POST /medias/upload` | [docs](https://robopost.app/docs/robopost-api/) |
| [Validate API Key](actions/validate-api-key.md) | `GET /auth/` | [docs](https://robopost.app/docs/robopost-api/) |
