# Get Clip Download URL with Restream

Generates a download URL for a clip in Restream.

## Endpoint

- **Method:** `GET`
- **Path:** `/user/clips/:clipId/download`
- **Base URL:** `https://api.restream.io/v2`
- **Official documentation:** [Get Clip Download URL](https://developers.restream.io/clips/clips-download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clipId` | path | `string` | yes | The ID of the clip whose download URL to retrieve. |
