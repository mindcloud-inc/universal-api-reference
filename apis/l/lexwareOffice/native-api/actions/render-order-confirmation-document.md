# Render Order Confirmation Document with Lexware Office

Retrieves a rendered order confirmation PDF from Lexware Office.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/order-confirmations/:id/document`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Render Order Confirmation Document](https://developers.lexware.io/docs/#order-confirmations-endpoint-render-an-order-confirmation-document-pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Lexware order confirmation ID. |
