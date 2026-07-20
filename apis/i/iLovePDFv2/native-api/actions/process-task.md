# Process Task with iLovePDFv2

Processes uploaded files for an iLovePDFv2 task.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:server/v1/process`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [Process Task](https://www.iloveapi.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `server` | path | `string` | yes | Processing server from Start Task. |
| `task` | body | `string` | yes | Task ID to process. |
| `tool` | body | `string` | yes | Tool used for this task. |
| `files[]` | body | `array<object>` | yes | Files array from upload results. |
