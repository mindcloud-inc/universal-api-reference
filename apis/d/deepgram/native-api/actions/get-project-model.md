# Get Project Model with Deepgram

Retrieves a project model from Deepgram.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/models/:model_id`
- **Base URL:** `https://api.deepgram.com`
- **Official documentation:** [Get Project Model](https://developers.deepgram.com/reference/manage/projects/models/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The Deepgram project identifier to inspect. |
| `model_id` | path | `string` | yes | The Deepgram model identifier to fetch. |
