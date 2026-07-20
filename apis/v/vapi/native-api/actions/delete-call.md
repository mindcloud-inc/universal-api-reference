# Delete Call with Vapi

Deletes an existing call from Vapi.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/call/:id`
- **Base URL:** `https://api.vapi.ai`
- **Official documentation:** [Delete Call](https://docs.vapi.ai/api-reference/calls/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `ids[]` | body | `array<string>` | no | These are the Call IDs to be bulk deleted. If provided, the call ID if any in the request query will be ignored When requesting a bulk delete, updates when a call is deleted will be sent as a webhook to the server URL configured in the Org settings. It may take up to a few hours to complete the bulk delete, and will be asynchronous. |
| `ids[]` | body | `array<string>` | no | These are the Call IDs to be bulk deleted. If provided, the call ID if any in the request query will be ignored When requesting a bulk delete, updates when a call is deleted will be sent as a webhook to the server URL configured in the Org settings. It may take up to a few hours to complete the bulk delete, and will be asynchronous. |
