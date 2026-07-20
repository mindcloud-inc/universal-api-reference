# Teyuto: Native API Reference

A consolidated summary of Teyuto's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.teyuto.com/
- **API base URL:** `https://api.teyuto.tv/v2`

## Authentication

### API Key

Use Teyuto's private auth token in the Authorization header together with the public channel key.

### Credentials

- **API Key:** `apiKey` · required
- **Channel:** `channel` · required · Public Teyuto channel key sent in the channel header.

Send these headers with each API request:

```http
channel: <channel>
Authorization: <apiKey>
```

[Official authentication documentation](https://docs.teyuto.com/api/teyuto)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://docs.teyuto.com/api/create-tag) |
| [Create User](actions/create-user.md) | `POST /users` | [docs](https://apidocs.teyuto.com/api-9259125) |
| [Delete Session](actions/delete-session.md) | `DELETE /sessions` | [docs](https://docs.teyuto.com/api/delete-session) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tags/:tag_id` | [docs](https://docs.teyuto.com/api/delete-tag) |
| [Delete User](actions/delete-user.md) | `DELETE /users/:user_id` | [docs](https://apidocs.teyuto.com/api-9259128) |
| [Generate Session](actions/generate-session.md) | `POST /sessions` | [docs](https://docs.teyuto.com/api/generate-session) |
| [Get Channel Settings](actions/get-channel-settings.md) | `GET /channel` | [docs](https://docs.teyuto.com/api/channel-settings) |
| [Get Collection](actions/get-collection.md) | `GET /collections/:collection_id` | [docs](https://apidocs.teyuto.com/api-9259098) |
| [Get Collections Analytics](actions/get-collections-analytics.md) | `GET /analytics/collections` | [docs](https://apidocs.teyuto.com/api-9259145) |
| [Get General Analytics](actions/get-general-analytics.md) | `GET /analytics/channel` | [docs](https://apidocs.teyuto.com/api-9259149) |
| [Get Tag](actions/get-tag.md) | `GET /tags/:tag_id` | [docs](https://docs.teyuto.com/api/get-tag) |
| [Get Video](actions/get-video.md) | `GET /videos/:video_id` | [docs](https://apidocs.teyuto.com/api-9259073) |
| [Get Videos Analytics](actions/get-videos-analytics.md) | `GET /analytics/videos` | [docs](https://apidocs.teyuto.com/api-9259147) |
| [List Collections](actions/list-collections.md) | `GET /collections` | [docs](https://apidocs.teyuto.com/api-9259096) |
| [List Packages](actions/list-packages.md) | `GET /packages` | [docs](https://apidocs.teyuto.com/api-9259109) |
| [List Restreams](actions/list-restreams.md) | `GET /restreams` | [docs](https://docs.teyuto.com/api/get-list-of-restreams) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://apidocs.teyuto.com/api-9259124) |
| [List Videos](actions/list-videos.md) | `GET /videos` | [docs](https://apidocs.teyuto.com/api-9259071) |
| [Update Tag](actions/update-tag.md) | `PATCH /tags/:tag_id` | [docs](https://docs.teyuto.com/api/edit-tag) |
