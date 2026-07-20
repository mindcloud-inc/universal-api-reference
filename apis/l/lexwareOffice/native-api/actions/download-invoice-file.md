# Download Invoice File with Lexware Office

Downloads an invoice file from Lexware Office.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/invoices/:id/file`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Download Invoice File](https://developers.lexware.io/docs/#invoices-endpoint-download-an-invoice-file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `*/*` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Lexware invoice ID. |
