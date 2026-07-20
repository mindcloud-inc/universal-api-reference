# Create Video Generation Job with Colossyan

Creates a new video generation job in Colossyan.

## Endpoint

- **Method:** `POST`
- **Path:** `/video-generation-jobs`
- **Base URL:** `https://app.colossyan.com/api/v1`
- **Official documentation:** [Create Video Generation Job](https://docs.colossyan.com/video-generation/video-generation/generating-a-video-manually)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoCreative` | body | `object` | yes | Full Colossyan videoCreative object describing settings and scenes. |
| `dynamicVariables` | body | `object` | no | Optional dynamic variables object used by the video job. |
| `callback` | body | `string` | no | Optional callback URL for job completion events. |
| `callbackPayload` | body | `object` | no | Optional callback payload object. |
