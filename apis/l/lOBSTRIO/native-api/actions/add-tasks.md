# Add Tasks with LOBSTR.IO

Creates new tasks in LOBSTR.IO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/tasks`
- **Base URL:** `https://api.lobstr.io`
- **Official documentation:** [Add Tasks](https://docs.lobstr.io/docs/add-tasks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `squid` | body | `string` | yes | The squid hash ID to add tasks to. |
| `tasks[]` | body | `array<object>` | yes | The array of task payloads to create. |
