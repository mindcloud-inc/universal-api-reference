# List Project Requests with Deepgram

Retrieves project requests from Deepgram.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/requests`
- **Base URL:** `https://api.deepgram.com`
- **Official documentation:** [List Project Requests](https://developers.deepgram.com/reference/manage/requests/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Deepgram project identifier. |
| `start` | query | `string` | no | Start of the requested date range in YYYY-MM-DD or ISO date-time format. |
| `end` | query | `string` | no | End of the requested date range in YYYY-MM-DD or ISO date-time format. |
| `accessor` | query | `string` | no | Filter request logs by accessor identifier. |
| `deployment` | query | `string` | no | Filter request logs by deployment: hosted, beta, or self-hosted. |
| `endpoint` | query | `string` | no | Filter request logs by endpoint: listen, read, speak, or agent. |
| `method` | query | `string` | no | Filter request logs by method: sync, async, or streaming. |
| `status` | query | `string` | no | Filter request logs by status: succeeded or failed. |
