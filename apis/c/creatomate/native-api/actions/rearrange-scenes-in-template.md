# Rearrange Scenes In Template with Creatomate

Creates a render with rearranged template scenes in Creatomate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/renders`
- **Base URL:** `https://api.creatomate.com`
- **Official documentation:** [Rearrange Scenes In Template](https://creatomate.com/docs/api/quick-start/rearrange-scenes-in-a-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | body | `string` | yes | Creatomate template ID to render from. |
| `sceneCopies[]` | body | `array<object>` | yes | Ordered scene copy instructions. Each object should include a `copy` scene name and any per-scene modifications from the template. |
