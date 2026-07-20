# Close Task with Morgen

Marks a task as completed in Morgen.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/tasks/close`
- **Base URL:** `https://api.morgen.so`
- **Official documentation:** [Close Task](https://docs.morgen.so/tasks#close-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Morgen task ID. |
| `occurrenceStart` | body | `string` | no | Specific occurrence start for recurring tasks. |
