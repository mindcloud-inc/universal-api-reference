# Create Idea with UserVitals

Creates a new idea in the roadmap API.

## Endpoint

- **Method:** `POST`
- **Path:** `/ideas`
- **Base URL:** `https://app.roadmap.space/v1`
- **Official documentation:** [Create Idea](https://api.roadmap.space/#create-idea)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | no | The idea category. |
| `desc` | body | `string` | no | The idea description. |
| `roadmapId` | body | `string` | yes | The roadmap id. |
| `title` | body | `string` | yes | The idea title. |
