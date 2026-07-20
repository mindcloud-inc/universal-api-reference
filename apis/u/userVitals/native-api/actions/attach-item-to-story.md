# Attach Item To Story with UserVitals

Attaches an idea or feedback item to a story.

## Endpoint

- **Method:** `POST`
- **Path:** `/stories/ideas`
- **Base URL:** `https://app.roadmap.space/v1`
- **Official documentation:** [Attach Item To Story](https://api.roadmap.space/#attach)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The feedback or idea id. |
| `parentId` | body | `string` | yes | The story id. |
| `roadmapId` | body | `string` | yes | The roadmap id. |
| `token` | body | `string` | yes | The feedback or idea token. |
