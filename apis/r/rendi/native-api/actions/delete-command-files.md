# Delete Command Files with Rendi

Deletes stored output files for a command in Rendi.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/commands/:command_id/files`
- **Base URL:** `https://api.rendi.dev`
- **Official documentation:** [Delete Command Files](https://docs.rendi.dev/api-reference/endpoint/delete-command-files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `command_id` | path | `string` | yes | UUID of the command whose stored files should be deleted. |
