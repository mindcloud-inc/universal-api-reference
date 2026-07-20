# Set Video Source with Vooplayer

Updates a video's source URL in Vooplayer.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/videoSource`
- **Base URL:** `https://api.spotlightr.com`
- **Official documentation:** [Set Video Source](https://app.spotlightr.com/docs/api/#videoSource)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | yes | Video source to be replaced. |
| `URL` | query | `string` | yes | New URL for the source. |
