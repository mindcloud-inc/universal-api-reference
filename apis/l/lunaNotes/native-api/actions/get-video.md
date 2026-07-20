# Get Video with LunaNotes

Retrieves a video from LunaNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/videos/:id`
- **Base URL:** `https://api.lunanotes.io`
- **Official documentation:** [Get Video](https://lunanotes.io/docs/videos/get-v1-videos-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The LunaNotes video ID. |
| `include` | query | `string` | no | Include related folder, transcripts, summaries, or notes in the response |
