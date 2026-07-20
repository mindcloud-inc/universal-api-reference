# List Videos with Vooplayer

Retrieves videos from Vooplayer by video or project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/videos`
- **Base URL:** `https://api.spotlightr.com`
- **Official documentation:** [List Videos](https://app.spotlightr.com/docs/api/#videos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoID` | query | `number` | no | ID of a video. |
| `videoGroup` | query | `number` | no | ID of a project. |
