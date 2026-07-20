# Connect Task with iLovePDFv2

Creates a follow-up task from an iLovePDFv2 task.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:server/v1/task/next`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [Connect Task](https://www.iloveapi.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `server` | path | `string` | yes | Processing server from parent task. |
| `task` | body | `string` | yes | Parent task ID. |
| `tool` | body | `string` | yes | Next tool to run. |
