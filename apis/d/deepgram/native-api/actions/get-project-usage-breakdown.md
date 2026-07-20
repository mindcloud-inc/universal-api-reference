# Get Project Usage Breakdown with Deepgram

Retrieves a project usage breakdown from Deepgram.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/usage/breakdown`
- **Base URL:** `https://api.deepgram.com`
- **Official documentation:** [Get Project Usage Breakdown](https://developers.deepgram.com/reference/manage/usage/breakdown/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Deepgram project identifier. |
| `start` | query | `string` | no | Start date for the requested usage-breakdown range in YYYY-MM-DD format. |
| `end` | query | `string` | no | End date for the requested usage-breakdown range in YYYY-MM-DD format. |
| `grouping` | query | `string` | no | Usage grouping dimension from the Deepgram reference. |
| `accessor` | query | `string` | no | Filter usage breakdown rows by accessor identifier. |
| `deployment` | query | `string` | no | Filter usage breakdown rows by deployment: hosted, beta, or self-hosted. |
| `endpoint` | query | `string` | no | Filter usage breakdown rows by endpoint: listen, read, speak, or agent. |
| `method` | query | `string` | no | Filter usage breakdown rows by method: sync, async, or streaming. |
| `model` | query | `string` | no | Filter usage breakdown rows by Deepgram model UUID. |
| `tag` | query | `string` | no | Filter usage breakdown rows by a specific tag. |
