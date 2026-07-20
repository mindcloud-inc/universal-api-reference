# Parse Switzerland QR-Bill Invoice with Invoice.xhub

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/invoice/CH/QR-BILL/parse`
- **Base URL:** `https://service.invoice-api.xhub.io`
- **Official documentation:** [Parse Switzerland QR-Bill Invoice](https://invoice-api.xhub.io/en/docs/api/parser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `string` | yes | Base64-encoded invoice document content. |
| `filename` | body | `string` | no | Optional filename for the encoded invoice document. |
