# <img src="https://images.mindcloud.co/apps/icons/favicon-1_1774891643248.png" alt="api.video logo" width="28" height="28"> api.video: Universal API

api.video provides APIs for video hosting, streaming, delivery, and analytics workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/apivideo/latest
- **Category:** Communication / Video Communications
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://api.video/
- **Vendor API docs:** https://docs.api.video/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List all video objects](actions/list-videos.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/list-videos?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Complete a live stream](actions/complete-a-live-stream.md) | PUT | Requests completion of a live stream in api.video. |
| [Create a player](actions/create-a-player.md) | POST | Creates a new player theme in api.video. |
| [Create a video object](actions/create-a-video-object.md) | POST | Creates a new video object in api.video. |
| [Create live stream](actions/create-live-stream.md) | POST | Creates a new live stream in api.video. |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in api.video. |
| [Delete a live stream](actions/delete-a-live-stream.md) | DELETE | Deletes a live stream from api.video. |
| [Delete a player](actions/delete-a-player.md) | DELETE | Deletes a player theme from api.video. |
| [Delete a video object](actions/delete-a-video-object.md) | DELETE | Deletes a video object from api.video. |
| [Delete a Webhook](actions/delete-a-webhook.md) | DELETE | Deletes an existing webhook from api.video. |
| [Delete an upload token](actions/delete-an-upload-token.md) | DELETE | Deletes an upload token from api.video. |
| [Delete video summary](actions/delete-video-summary.md) | DELETE | Deletes a video summary from api.video. |
| [Generate an upload token](actions/generate-an-upload-token.md) | POST | Creates a new upload token in api.video. |
| [Generate video summary](actions/generate-video-summary.md) | POST | Creates a new video summary in api.video. |
| [Get Bearer Token](actions/get-bearer-token.md) | POST | Retrieves a bearer token from api.video. |
| [Get summary details](actions/get-summary-details.md) | GET | Retrieves summary source details from api.video. |
| [List all active upload tokens](actions/list-all-active-upload-tokens.md) | GET | Retrieves active delegated upload tokens from api.video. |
| [List all live streams](actions/list-all-live-streams.md) | GET | Retrieves all live streams from api.video. |
| [List all player themes](actions/list-all-player-themes.md) | GET | Retrieves all player themes from api.video. |
| [List all video tags](actions/list-all-video-tags.md) | GET | Retrieves video tags and usage counts from api.video. |
| [List all webhooks](actions/list-all-webhooks.md) | GET | Retrieves all webhook records from api.video. |
| [List summaries](actions/list-summaries.md) | GET | Retrieves all video summaries from api.video. |
| [List all video objects](actions/list-videos.md) | GET | Retrieves all video objects from api.video. |
| [Refresh Bearer Token](actions/refresh-bearer-token.md) | POST | Refreshes a bearer token for api.video. |
| [Retrieve a player](actions/retrieve-a-player.md) | GET | Retrieves a player theme from api.video. |
| [Retrieve a video object](actions/retrieve-a-video-object.md) | GET | Retrieves a video object from api.video. |
| [Retrieve aggregated metrics](actions/retrieve-aggregated-metrics.md) | GET | Retrieves aggregated analytics metrics from api.video. |
| [Retrieve live stream](actions/retrieve-live-stream.md) | GET | Retrieves a live stream from api.video. |
| [Retrieve metrics in a breakdown of dimensions](actions/retrieve-metrics-in-a-breakdown-of-dimensions.md) | GET | Retrieves analytics metrics by dimension from api.video. |
| [Retrieve metrics over time](actions/retrieve-metrics-over-time.md) | GET | Retrieves analytics metrics over time from api.video. |
| [Retrieve upload token](actions/retrieve-upload-token.md) | GET | Retrieves an upload token from api.video. |
| [Retrieve video status and details](actions/retrieve-video-status-and-details.md) | GET | Retrieves video status and details from api.video. |
| [Retrieve Webhook details](actions/retrieve-webhook-details.md) | GET | Retrieves detailed webhook information from api.video. |
| [Update a live stream](actions/update-a-live-stream.md) | PUT | Updates an existing live stream in api.video. |
| [Update a player](actions/update-a-player.md) | PUT | Updates an existing player theme in api.video. |
| [Update a video object](actions/update-a-video-object.md) | PUT | Updates an existing video object in api.video. |
| [Update summary details](actions/update-summary-details.md) | PUT | Updates summary source details in api.video. |

