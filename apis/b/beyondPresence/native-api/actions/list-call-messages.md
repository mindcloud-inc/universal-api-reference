# List Call Messages with Beyond Presence

Retrieves transcribed messages from a Beyond Presence call.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/calls/:id/messages`
- **Base URL:** `https://api.bey.dev`
- **Official documentation:** [List Call Messages](https://docs.bey.dev/api-reference/calls/list-call-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Call ID. |
