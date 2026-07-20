# List Project Models with Deepgram

Retrieves project models from Deepgram.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/models`
- **Base URL:** `https://api.deepgram.com`
- **Official documentation:** [List Project Models](https://developers.deepgram.com/reference/manage/projects/models/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The Deepgram project identifier to inspect. |
| `include_outdated` | query | `boolean` | no | Whether to include non-latest project model versions. |
