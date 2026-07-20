# Create Idea with Stormboard

Creates an idea in Stormboard.

## Endpoint

- **Method:** `POST`
- **Path:** `/ideas`
- **Base URL:** `https://api.stormboard.com`
- **Official documentation:** [Create Idea](https://api.stormboard.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `string` | no | Idea color. |
| `data` | body | `string` | yes | Idea content, media URL, or base64 file data depending on the idea type. |
| `lock` | body | `number` | no | Set to 1 to lock the idea, or 0 to leave it unlocked. |
| `name` | body | `string` | no | Name for a video, whiteboard, image, or document idea. |
| `sectionindex` | body | `string` | no | Place the idea inside a section by index. |
| `shape` | body | `string` | no | Idea shape. |
| `stormid` | body | `number` | yes | Storm ID where the new idea should be created. |
| `type` | body | `string` | no | Idea type: text, indexcard, image, video, document, or whiteboard. |
| `x` | body | `number` | no | X position for the new idea. |
| `y` | body | `number` | no | Y position for the new idea. |
