# Synchronize Multiple Elements with Creatomate

Creates a render that synchronizes multiple elements.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/renders`
- **Base URL:** `https://api.creatomate.com`
- **Official documentation:** [Synchronize Multiple Elements](https://creatomate.com/docs/api/quick-start/synchronize-multiple-elements)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `videoUrls[]` | body | `array<string>` | yes | Ordered list of video URLs that define the primary timeline. |
| `musicUrl` | body | `string` | no | Optional music track that should stop when the video timeline ends. |
| `overlayText` | body | `string` | no | Optional text overlay that should stretch across the full timeline. |
| `audioFadeOutSeconds` | body | `number` | no | Fade-out duration for the synchronized music track. |
