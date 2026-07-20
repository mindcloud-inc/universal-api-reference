# VideoDB: Native API Reference

A consolidated summary of VideoDB's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://docs.videodb.io/api-reference/introduction
- **API base URL:** `https://api.videodb.io`

## Authentication

### API Key

Connect with a VideoDB API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-access-token: <apiKey>
```

[Official authentication documentation](https://docs.videodb.io/pages/getting-started/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `count` in the query string to set the page size (default 50; maximum 5000). Use `page_index` in the query string to choose the page; numbering starts at 0.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | `POST /collection` | [docs](https://docs.videodb.io/api-reference/collections/create_collection) |
| [Delete Collection](actions/delete-collection.md) | `DELETE /collection/:collection_id` | [docs](https://docs.videodb.io/api-reference/collections/delete_collection) |
| [Delete Video](actions/delete-video.md) | `DELETE /video/:video_id` | [docs](https://docs.videodb.io/api-reference/videos/delete_video) |
| [Get Collection](actions/get-collection.md) | `GET /collection/:collection_id` | [docs](https://docs.videodb.io/api-reference/collections/get_collection) |
| [Get Video Details](actions/get-video-details.md) | `GET /video/:video_id` | [docs](https://docs.videodb.io/api-reference/videos/get_video) |
| [Get Video Transcription](actions/get-video-transcription.md) | `GET /video/:video_id/transcription/` | [docs](https://docs.videodb.io/api-reference/videos/transcription/get_video_transcription) |
| [List Collections](actions/list-collections.md) | `GET /collection/` | [docs](https://docs.videodb.io/api-reference/collections/list_collections) |
| [List Videos](actions/list-videos.md) | `GET /video/` | [docs](https://docs.videodb.io/api-reference/videos/list_videos) |
| [Update Collection](actions/update-collection.md) | `PATCH /collection/:collection_id` | [docs](https://docs.videodb.io/api-reference/collections/update_collection) |
| [Update Video](actions/update-video.md) | `PATCH /video/:video_id` | [docs](https://docs.videodb.io/api-reference/videos/update_video) |
| [Upload to Collection](actions/upload-to-collection.md) | `POST /collection/:collection_id/upload` | [docs](https://docs.videodb.io/api-reference/collections/upload_to_collection) |
