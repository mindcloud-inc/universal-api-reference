# Generate France Factur-X Invoice with Invoice.xhub

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/invoice/FR/FACTURX/generate`
- **Base URL:** `https://service.invoice-api.xhub.io`
- **Official documentation:** [Generate France Factur-X Invoice](https://invoice-api.xhub.io/en/docs/api/creator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `invoice` | body | `object` | yes | Invoice payload to generate the document from. |
| `formatOptions` | body | `object` | no | Optional format-specific generation options. |
