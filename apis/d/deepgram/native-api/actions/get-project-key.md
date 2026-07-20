# Get Project Key with Deepgram

Retrieves a project API key from Deepgram.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/keys/:key_id`
- **Base URL:** `https://api.deepgram.com`
- **Official documentation:** [Get Project Key](https://developers.deepgram.com/reference/manage/keys/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The Deepgram project identifier to inspect. |
| `key_id` | path | `string` | yes | The Deepgram API key identifier to fetch. |
