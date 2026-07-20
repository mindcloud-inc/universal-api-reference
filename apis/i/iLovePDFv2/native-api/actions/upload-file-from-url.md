# Upload File From URL with iLovePDFv2

Uploads a file to an iLovePDFv2 task from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `https://:server/v1/upload`
- **Base URL:** `https://api.ilovepdf.com/v1`
- **Official documentation:** [Upload File From URL](https://www.iloveapi.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `server` | path | `string` | yes | Processing server from Start Task. |
| `task` | body | `string` | yes | Task ID from Start Task. |
| `cloud_file` | body | `string` | yes | Public URL for the source file to upload. |
