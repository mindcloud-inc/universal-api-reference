# Update Call Flow with CallScaler

Updates a call flow in CallScaler.

## Endpoint

- **Method:** `PUT`
- **Path:** `/call-flows/:id`
- **Base URL:** `https://callscaler.com/api/v1`
- **Official documentation:** [Update Call Flow](https://callscaler.com/docs/api-resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `name` | body | `string` | no | — |
| `settings` | body | `object` | no | Call-flow settings such as recording, whisper, and press1. |
| `steps[]` | body | `array<object>` | no | Call-flow step configuration. |
