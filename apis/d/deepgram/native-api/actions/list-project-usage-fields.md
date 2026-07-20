# List Project Usage Fields with Deepgram

Retrieves project usage fields from Deepgram.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/usage/fields`
- **Base URL:** `https://api.deepgram.com`
- **Official documentation:** [List Project Usage Fields](https://developers.deepgram.com/reference/manage/usage/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Deepgram project identifier. |
| `start` | query | `string` | no | Start date for the requested usage-field range in YYYY-MM-DD format. |
| `end` | query | `string` | no | End date for the requested usage-field range in YYYY-MM-DD format. |
