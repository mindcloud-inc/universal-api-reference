# Update Video Player Settings with Vooplayer

Updates video player settings in Vooplayer.

## Endpoint

- **Method:** `POST`
- **Path:** `/video/updateSettings`
- **Base URL:** `https://api.spotlightr.com`
- **Official documentation:** [Update Video Player Settings](https://app.spotlightr.com/docs/api/#updatePlayerSettings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `number` | yes | Video ID as the base64 decoded value. |
| `settings` | body | `object` | yes | Object containing only the keys to update. |
