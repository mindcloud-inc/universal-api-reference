# Download Quotation File with Lexware Office

Downloads a quotation file from Lexware Office.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/quotations/:id/file`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Download Quotation File](https://developers.lexware.io/docs/#quotations-endpoint-download-a-quotation-file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `*/*` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Lexware quotation ID. |
