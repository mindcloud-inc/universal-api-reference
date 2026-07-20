# Create Call Flow with CallScaler

Creates a call flow in CallScaler.

## Endpoint

- **Method:** `POST`
- **Path:** `/call-flows`
- **Base URL:** `https://callscaler.com/api/v1`
- **Official documentation:** [Create Call Flow](https://callscaler.com/docs/api-resources)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `settings` | body | `object` | no | Call-flow settings such as recording, whisper, and press1. |
| `steps[]` | body | `array<object>` | no | Call-flow step configuration. |
