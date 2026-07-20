# Create Feedback with UserVitals

Creates a new feedback item in the roadmap API.

## Endpoint

- **Method:** `POST`
- **Path:** `/feedback`
- **Base URL:** `https://app.roadmap.space/v1`
- **Official documentation:** [Create Feedback](https://api.roadmap.space/#create-feedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roadmapId` | body | `string` | yes | The roadmap id. |
| `title` | body | `string` | yes | The feedback title. |
