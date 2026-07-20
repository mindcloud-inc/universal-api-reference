# Update Number with CallScaler

Updates a number in CallScaler.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/numbers/:id`
- **Base URL:** `https://callscaler.com/api/v1`
- **Official documentation:** [Update Number](https://callscaler.com/docs/api-resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `call_flow_id` | body | `string` | no | Call flow to assign to the number. |
| `friendly_name` | body | `string` | no | New display name for the tracking number. |
| `id` | path | `string` | yes | — |
