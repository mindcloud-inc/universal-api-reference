# Create Bulk Validation List with validTo

Creates a bulk validation list in validTo.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulk`
- **Base URL:** `https://api.validto.com/v1`
- **Official documentation:** [Create Bulk Validation List](https://validto.readme.io/reference/create-a-bulk-validation-list)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `local_file` | body | `file` | yes | — |
| `auto_verify` | body | `boolean` | no | Automatically start verification after upload when supported. |
