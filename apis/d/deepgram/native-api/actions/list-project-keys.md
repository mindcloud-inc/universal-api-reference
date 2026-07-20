# List Project Keys with Deepgram

Retrieves project API keys from Deepgram.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/keys`
- **Base URL:** `https://api.deepgram.com`
- **Official documentation:** [List Project Keys](https://developers.deepgram.com/reference/manage/keys/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The Deepgram project identifier to inspect. |
| `status` | query | `string` | no | Filter returned keys by Deepgram key status (`active` or `expired`). Accepted values: `0`, `1`. |
