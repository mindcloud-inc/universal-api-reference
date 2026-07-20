# Update Feedback with UserVitals

Updates an existing feedback item in the roadmap API.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ideas`
- **Base URL:** `https://app.roadmap.space/v1`
- **Official documentation:** [Update Feedback](https://api.roadmap.space/#update-feedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `desc` | body | `string` | no | The updated description. |
| `id` | body | `string` | yes | The feedback id. |
| `roadmapId` | body | `string` | yes | The roadmap id. |
| `title` | body | `string` | no | The updated title. |
| `token` | body | `string` | yes | The feedback token. |
