# Group Elements Into Scenes with Creatomate

Creates a render that groups elements into scenes.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/renders`
- **Base URL:** `https://api.creatomate.com`
- **Official documentation:** [Group Elements Into Scenes](https://creatomate.com/docs/api/quick-start/group-elements-into-scenes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scenes[]` | body | `array<object>` | yes | Ordered list of scene objects. Each scene should include `audioSource` and `imageSource`. |
| `logoOverlayUrl` | body | `string` | no | Optional logo image URL to overlay across every scene. |
