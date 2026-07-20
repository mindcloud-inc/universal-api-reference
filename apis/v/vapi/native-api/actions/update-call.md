# Update Call with Vapi

Updates an existing call in Vapi.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/call/:id`
- **Base URL:** `https://api.vapi.ai`
- **Official documentation:** [Update Call](https://docs.vapi.ai/api-reference/calls/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `name` | body | `string` | no | This is the name of the call. This is just for your own reference. |
