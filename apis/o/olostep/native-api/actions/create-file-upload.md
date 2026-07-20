# Create File Upload with Olostep

Creates a new file upload in Olostep.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/files`
- **Base URL:** `https://api.olostep.com`
- **Official documentation:** [Create File Upload](https://docs.olostep.com/api-reference/files/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `string` | yes | The JSON filename to register before uploading file bytes. |
| `purpose` | body | `string` | no | Why you are uploading this file. Accepted values: `0`. |
