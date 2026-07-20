# Render Quotation Document with Lexware Office

Retrieves a rendered quotation PDF from Lexware Office.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/quotations/:id/document`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Render Quotation Document](https://developers.lexware.io/docs/#quotations-endpoint-render-a-quotation-document-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Lexware quotation ID. |
