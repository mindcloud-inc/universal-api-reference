# Get Project Balance with Deepgram

Retrieves a project balance from Deepgram.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/balances/:balance_id`
- **Base URL:** `https://api.deepgram.com`
- **Official documentation:** [Get Project Balance](https://developers.deepgram.com/reference/manage/billing/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Deepgram project identifier. |
| `balance_id` | path | `string` | yes | Deepgram balance identifier. |
