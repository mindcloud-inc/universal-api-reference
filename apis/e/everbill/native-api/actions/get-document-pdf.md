# Get Document PDF with Everbill

Retrieves a document PDF from Everbill.

## Endpoint

- **Method:** `GET`
- **Path:** `/:document_name/get_pdf/:document_number`
- **Base URL:** `https://api.everbill.eu`
- **Official documentation:** [Get Document PDF](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1{document_name}~1get_pdf~1{document_number}/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_name` | path | `string` | yes | Document type path segment, for example bills, offers, orders, or incoming_bills. |
| `document_number` | path | `string` | yes | Everbill document number. |
