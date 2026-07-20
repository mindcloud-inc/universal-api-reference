# Reopen Task with Morgen

Reopens a completed task in Morgen.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/tasks/reopen`
- **Base URL:** `https://api.morgen.so`
- **Official documentation:** [Reopen Task](https://docs.morgen.so/tasks#reopen-a-task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Morgen task ID. |
| `occurrenceStart` | body | `string` | no | Specific occurrence start for recurring tasks. |
