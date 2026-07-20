# Update Story with UserVitals

Updates an existing story in the roadmap API.

## Endpoint

- **Method:** `PUT`
- **Path:** `/stories`
- **Base URL:** `https://app.roadmap.space/v1`
- **Official documentation:** [Update Story](https://api.roadmap.space/#update-story)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `desc` | body | `string` | no | The updated description. |
| `id` | body | `string` | yes | The story id. |
| `roadmapId` | body | `string` | yes | The roadmap id. |
| `title` | body | `string` | no | The updated title. |
| `token` | body | `string` | yes | The story token. |
