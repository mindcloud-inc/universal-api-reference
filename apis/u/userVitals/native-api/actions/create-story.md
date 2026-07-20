# Create Story with UserVitals

Creates a new story in the roadmap API.

## Endpoint

- **Method:** `POST`
- **Path:** `/stories`
- **Base URL:** `https://app.roadmap.space/v1`
- **Official documentation:** [Create Story](https://api.roadmap.space/#create-story)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `desc` | body | `string` | no | The story description. |
| `roadmapId` | body | `string` | yes | The roadmap id. |
| `title` | body | `string` | yes | The story title. |
