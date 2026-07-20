# Download File with Lexware Office

Downloads a bookkeeping voucher file from Lexware Office.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/files/:id`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Download File](https://developers.lexware.io/docs/#files-endpoint-download-a-file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `*/*` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Lexware file ID. |
