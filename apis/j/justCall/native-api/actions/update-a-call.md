# Update a Call with JustCall

Updates an existing call in JustCall.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2.1/calls/:id`
- **Base URL:** `https://api.justcall.io`
- **Official documentation:** [Update a Call](https://developer.justcall.io/reference/call_update_v21)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The JustCall call ID or SID. |
| `notes` | body | `string` | no | Updated notes for the completed call. |
