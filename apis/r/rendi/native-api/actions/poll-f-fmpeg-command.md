# Poll FFmpeg Command with Rendi

Retrieves the status of an FFmpeg command in Rendi.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/commands/:command_id`
- **Base URL:** `https://api.rendi.dev`
- **Official documentation:** [Poll FFmpeg Command](https://docs.rendi.dev/api-reference/endpoint/poll-command)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `command_id` | path | `string` | yes | UUID of the FFmpeg command to fetch current status for. |
