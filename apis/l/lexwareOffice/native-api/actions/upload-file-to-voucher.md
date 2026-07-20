# Upload File to Voucher with Lexware Office

Uploads a file to a voucher in Lexware Office.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/vouchers/:id/files`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Upload File to Voucher](https://developers.lexware.io/docs/#vouchers-endpoint-upload-a-file-to-a-voucher)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Voucher ID from Lexware. |
| `file` | body | `file` | yes | PDF, image, or XML file content to attach. |
