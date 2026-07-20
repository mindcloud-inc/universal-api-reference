# Get Call Details with Ringg AI

Retrieves call details from Ringg AI.

## Endpoint

- **Method:** `GET`
- **Path:** `/calling/call-details`
- **Base URL:** `https://prod-api.ringg.ai/ca/api/v0`
- **Official documentation:** [Get Call Details](https://docs.ringg.ai/api-reference/endpoint/history/get-call-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | (Required) The unique identifier (UUID) of the call. |
| `send_analysis` | query | `boolean` | no | (Optional) Whether to include analysis data (platform_analysis and client_analysis) in the response. |
