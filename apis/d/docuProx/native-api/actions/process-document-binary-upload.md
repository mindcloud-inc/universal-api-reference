# Process Document Binary Upload with DocuProx

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/process`
- **Base URL:** `https://api.docuprox.com`
- **Official documentation:** [Process Document Binary Upload](https://docuprox.com/docs/api/#process-endpoint)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `t_id` | query | `string` | yes | UUID of the DocuProx template to use. |
| `documentFile` | body | `file` | yes | Binary document stream uploaded as the raw request body. |
