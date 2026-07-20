# Download Task Result with iLovePDFv2

Downloads output files for an iLovePDFv2 task.

## Endpoint

- **Method:** `GET`
- **Path:** `https://:server/v1/download/:task`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [Download Task Result](https://www.iloveapi.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `server` | path | `string` | yes | Processing server from Start Task. |
| `task` | path | `string` | yes | Task ID to download. |
