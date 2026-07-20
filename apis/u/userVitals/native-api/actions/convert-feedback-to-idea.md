# Convert Feedback To Idea with UserVitals

Converts a feedback item to an idea.

## Endpoint

- **Method:** `PUT`
- **Path:** `/feedback/convert`
- **Base URL:** `https://app.roadmap.space/v1`
- **Official documentation:** [Convert Feedback To Idea](https://api.roadmap.space/#convert-feedback-to-idea)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | The feedback id. |
| `roadmapId` | body | `string` | yes | The roadmap id. |
| `token` | body | `string` | yes | The feedback token. |
