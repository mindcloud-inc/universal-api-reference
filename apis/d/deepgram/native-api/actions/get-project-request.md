# Get Project Request with Deepgram

Retrieves a project request from Deepgram.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/requests/:request_id`
- **Base URL:** `https://api.deepgram.com`
- **Official documentation:** [Get Project Request](https://developers.deepgram.com/reference/manage/requests/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Deepgram project identifier. |
| `request_id` | path | `string` | yes | Deepgram request identifier. |
