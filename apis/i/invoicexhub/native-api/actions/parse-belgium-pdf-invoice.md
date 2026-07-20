# Parse Belgium PDF Invoice with Invoice.xhub

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/invoice/BE/pdf/parse`
- **Base URL:** `https://service.invoice-api.xhub.io`
- **Official documentation:** [Parse Belgium PDF Invoice](https://invoice-api.xhub.io/en/docs/api/parser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `string` | yes | Encoded invoice payload to parse. |
| `filename` | body | `string` | no | Optional original filename for format detection hints. |
