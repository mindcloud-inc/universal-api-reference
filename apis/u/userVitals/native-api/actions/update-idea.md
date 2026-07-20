# Update Idea with UserVitals

Updates an existing idea in the roadmap API.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ideas`
- **Base URL:** `https://app.roadmap.space/v1`
- **Official documentation:** [Update Idea](https://api.roadmap.space/#update-idea)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `desc` | body | `string` | no | The updated description. |
| `id` | body | `string` | yes | The idea id. |
| `roadmapId` | body | `string` | yes | The roadmap id. |
| `title` | body | `string` | no | The updated title. |
| `token` | body | `string` | yes | The idea token. |
