# Render Invoice Document with Lexware Office

Retrieves a rendered invoice PDF from Lexware Office.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/invoices/:id/document`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Render Invoice Document](https://developers.lexware.io/docs/#invoices-endpoint-render-an-invoice-document-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Lexware invoice ID. |
