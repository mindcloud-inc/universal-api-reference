# api.video: Native API Reference

A consolidated summary of api.video's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://docs.api.video/reference
- **API base URL:** `https://ws.api.video`

## Authentication

### Bearer Token (API Key Exchange)

Custom auth for api.video bearer tokens derived from the API-key exchange endpoint.

### Credentials

- **API Key:** `apiKey` · required · Your api.video API key from the api.video dashboard.

Send these headers with each API request:

```http
Authorization: Bearer <custom.access_token>
```

[Official authentication documentation](https://docs.api.video/reference/authentication-guide)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Complete a live stream](actions/complete-a-live-stream.md) | `PUT /live-streams/:liveStreamId/complete` | [docs](https://docs.api.video/reference/api/Live-Streams#complete-a-live-stream) |
| [Create a player](actions/create-a-player.md) | `POST /players` | [docs](https://docs.api.video/reference/api/Player-Themes#create-a-player) |
| [Create a video object](actions/create-a-video-object.md) | `POST /videos` | [docs](https://docs.api.video/reference/api/Videos#create-a-video-object) |
| [Create live stream](actions/create-live-stream.md) | `POST /live-streams` | [docs](https://docs.api.video/reference/api/Live-Streams#create-live-stream) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://docs.api.video/reference/api/Webhooks#create-webhook) |
| [Delete a live stream](actions/delete-a-live-stream.md) | `DELETE /live-streams/:liveStreamId` | [docs](https://docs.api.video/reference/api/Live-Streams#delete-a-live-stream) |
| [Delete a player](actions/delete-a-player.md) | `DELETE /players/:playerId` | [docs](https://docs.api.video/reference/api/Player-Themes#delete-a-player) |
| [Delete a video object](actions/delete-a-video-object.md) | `DELETE /videos/:videoId` | [docs](https://docs.api.video/reference/api/Videos#delete-a-video-object) |
| [Delete a Webhook](actions/delete-a-webhook.md) | `DELETE /webhooks/:webhookId` | [docs](https://docs.api.video/reference/api/Webhooks#delete-a-webhook) |
| [Delete an upload token](actions/delete-an-upload-token.md) | `DELETE /upload-tokens/:uploadToken` | [docs](https://docs.api.video/reference/api/Upload-Tokens#delete-an-upload-token) |
| [Delete video summary](actions/delete-video-summary.md) | `DELETE /summaries/:summaryId` | [docs](https://docs.api.video/reference/api/Summaries#delete-video-summary) |
| [Generate an upload token](actions/generate-an-upload-token.md) | `POST /upload-tokens` | [docs](https://docs.api.video/reference/api/Upload-Tokens#generate-an-upload-token) |
| [Generate video summary](actions/generate-video-summary.md) | `POST /summaries` | [docs](https://docs.api.video/reference/api/Summaries#generate-video-summary) |
| [Get Bearer Token](actions/get-bearer-token.md) | `POST /auth/api-key` | [docs](https://docs.api.video/reference/api/Advanced-authentication#get-bearer-token) |
| [Get summary details](actions/get-summary-details.md) | `GET /summaries/:summaryId/source` | [docs](https://docs.api.video/reference/api/Summaries#get-summary-details) |
| [List all active upload tokens](actions/list-all-active-upload-tokens.md) | `GET /upload-tokens` | [docs](https://docs.api.video/reference/api/Upload-Tokens#list-all-active-upload-tokens) |
| [List all live streams](actions/list-all-live-streams.md) | `GET /live-streams` | [docs](https://docs.api.video/reference/api/Live-Streams#list-all-live-streams) |
| [List all player themes](actions/list-all-player-themes.md) | `GET /players` | [docs](https://docs.api.video/reference/api/Player-Themes#list-all-player-themes) |
| [List all video tags](actions/list-all-video-tags.md) | `GET /tags` | [docs](https://docs.api.video/reference/api/Tags#list-all-video-tags) |
| [List all webhooks](actions/list-all-webhooks.md) | `GET /webhooks` | [docs](https://docs.api.video/reference/api/Webhooks#list-all-webhooks) |
| [List summaries](actions/list-summaries.md) | `GET /summaries` | [docs](https://docs.api.video/reference/api/Summaries#list-summaries) |
| [List all video objects](actions/list-videos.md) | `GET /videos` | [docs](https://docs.api.video/reference/api/Videos#list-all-video-objects) |
| [Refresh Bearer Token](actions/refresh-bearer-token.md) | `POST /auth/refresh` | [docs](https://docs.api.video/reference/api/Advanced-authentication#refresh-bearer-token) |
| [Retrieve a player](actions/retrieve-a-player.md) | `GET /players/:playerId` | [docs](https://docs.api.video/reference/api/Player-Themes#retrieve-a-player) |
| [Retrieve a video object](actions/retrieve-a-video-object.md) | `GET /videos/:videoId` | [docs](https://docs.api.video/reference/api/Videos#retrieve-a-video-object) |
| [Retrieve aggregated metrics](actions/retrieve-aggregated-metrics.md) | `GET /data/metrics/:metric/:aggregation` | [docs](https://docs.api.video/reference/api/Analytics#retrieve-aggregated-metrics) |
| [Retrieve live stream](actions/retrieve-live-stream.md) | `GET /live-streams/:liveStreamId` | [docs](https://docs.api.video/reference/api/Live-Streams#retrieve-live-stream) |
| [Retrieve metrics in a breakdown of dimensions](actions/retrieve-metrics-in-a-breakdown-of-dimensions.md) | `GET /data/buckets/:metric/:breakdown` | [docs](https://docs.api.video/reference/api/Analytics#retrieve-metrics-in-a-breakdown-of-dimensions) |
| [Retrieve metrics over time](actions/retrieve-metrics-over-time.md) | `GET /data/timeseries/:metric` | [docs](https://docs.api.video/reference/api/Analytics#retrieve-metrics-over-time) |
| [Retrieve upload token](actions/retrieve-upload-token.md) | `GET /upload-tokens/:uploadToken` | [docs](https://docs.api.video/reference/api/Upload-Tokens#retrieve-upload-token) |
| [Retrieve video status and details](actions/retrieve-video-status-and-details.md) | `GET /videos/:videoId/status` | [docs](https://docs.api.video/reference/api/Videos#retrieve-video-status-and-details) |
| [Retrieve Webhook details](actions/retrieve-webhook-details.md) | `GET /webhooks/:webhookId` | [docs](https://docs.api.video/reference/api/Webhooks#retrieve-webhook-details) |
| [Update a live stream](actions/update-a-live-stream.md) | `PATCH /live-streams/:liveStreamId` | [docs](https://docs.api.video/reference/api/Live-Streams#update-a-live-stream) |
| [Update a player](actions/update-a-player.md) | `PATCH /players/:playerId` | [docs](https://docs.api.video/reference/api/Player-Themes#update-a-player) |
| [Update a video object](actions/update-a-video-object.md) | `PATCH /videos/:videoId` | [docs](https://docs.api.video/reference/api/Videos#update-a-video-object) |
| [Update summary details](actions/update-summary-details.md) | `PATCH /summaries/:summaryId/source` | [docs](https://docs.api.video/reference/api/Summaries#update-summary-details) |
