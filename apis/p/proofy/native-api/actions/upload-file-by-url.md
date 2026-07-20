# Upload File by URL with Proofy

## Endpoint

- **Method:** `POST`
- **Path:** `/verify/file/create`
- **Base URL:** `https://apis.proofy.io/v1`
- **Official documentation:** [Upload File by URL](https://docs.proofy.io/api-reference/endpoint/verify-file-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_name` | body | `string` | yes | Name to assign to the uploaded file task. |
| `file_url` | body | `string` | yes | Public URL for the file containing email addresses. |
