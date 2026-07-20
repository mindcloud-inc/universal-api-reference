# Get Project Usage with Deepgram

Retrieves project usage from Deepgram.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/usage`
- **Base URL:** `https://api.deepgram.com`
- **Official documentation:** [Get Project Usage](https://developers.deepgram.com/reference/manage/usage/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Deepgram project identifier. |
| `start` | query | `string` | no | Start date for the requested usage range in YYYY-MM-DD format. |
| `end` | query | `string` | no | End date for the requested usage range in YYYY-MM-DD format. |
| `accessor` | query | `string` | no | Filter usage rows by accessor identifier. |
| `deployment` | query | `string` | no | Filter usage rows by deployment: hosted, beta, or self-hosted. |
| `endpoint` | query | `string` | no | Filter usage rows by endpoint: listen, read, speak, or agent. |
| `method` | query | `string` | no | Filter usage rows by method: sync, async, or streaming. |
| `model` | query | `string` | no | Filter usage rows by Deepgram model UUID. |
| `tag` | query | `string` | no | Filter usage rows by a specific tag. |
