# Create Video with Vooplayer

Creates a new video in Vooplayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/createVideo`
- **Base URL:** `https://api.spotlightr.com`
- **Official documentation:** [Create Video](https://app.spotlightr.com/docs/api/#create-video)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Video name. |
| `URL` | body | `string` | no | Video URL. |
| `file` | body | `file` | no | File to upload. |
| `customS3` | body | `number` | yes | 0 or ID of custom integration. |
| `hls` | body | `number` | no | 1 to encode or 0 to leave as unsecured. |
| `videoGroup` | body | `number` | no | Project ID. |
| `playerSettings` | body | `object` | no | Video ID for copying player settings, decoded base64. |
| `create` | body | `number` | no | 1 to confirm or 0 to debug. |
