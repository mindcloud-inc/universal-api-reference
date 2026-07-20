# Move Idea with UserVitals

Moves an idea to another roadmap state.

## Endpoint

- **Method:** `POST`
- **Path:** `/ideas/move/:type`
- **Base URL:** `https://app.roadmap.space/v1`
- **Official documentation:** [Move Idea](https://api.roadmap.space/#move-to-widget-idea-active)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The idea id. |
| `roadmapId` | body | `string` | yes | The roadmap id. |
| `token` | body | `string` | yes | The idea token. |
| `type` | path | `string` | yes | The destination state: widget, idea, or active. |
