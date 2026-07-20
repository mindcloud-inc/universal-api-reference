# Run Task with Skyvern

Runs a browser automation task in Skyvern.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/run/tasks`
- **Base URL:** `https://api.skyvern.com`
- **Official documentation:** [Run Task](https://www.skyvern.com/docs/api-reference/agent/run-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prompt` | body | `string` | yes | The goal or task description for Skyvern to accomplish. |
| `url` | body | `string` | no | The starting URL for the task. |
