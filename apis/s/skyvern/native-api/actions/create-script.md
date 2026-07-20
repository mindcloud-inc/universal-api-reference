# Create Script with Skyvern

Creates a new script in Skyvern.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/scripts`
- **Base URL:** `https://api.skyvern.com`
- **Official documentation:** [Create Script](https://www.skyvern.com/docs/api-reference/scripts/create-script)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `files` | body | `string` | no | Array of files to include in the script |
| `run_id` | body | `string` | no | Associated run ID |
| `workflow_id` | body | `string` | no | Associated workflow ID |
