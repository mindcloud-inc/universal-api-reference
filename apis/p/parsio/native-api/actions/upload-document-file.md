# Upload Document File with Parsio

## Endpoint

- **Method:** `POST`
- **Path:** `/mailboxes/:mailbox_id/upload`
- **Base URL:** `https://api.parsio.io`
- **Official documentation:** [Upload Document File](https://help.parsio.io/public-api/parse-pdf-and-files-using-api-1)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mailbox_id` | path | `string` | yes | Parsio mailbox ID. |
| `file` | body | `file` | yes | File binary payload to upload. |
| `meta` | body | `object` | no | Optional metadata object included as __meta__ in parsed output. |
