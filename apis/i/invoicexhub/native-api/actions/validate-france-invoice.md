# Validate France Invoice with Invoice.xhub

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/invoice/FR/validate`
- **Base URL:** `https://service.invoice-api.xhub.io`
- **Official documentation:** [Validate France Invoice](https://invoice-api.xhub.io/en/docs/api/validator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `xml` | body | `string` | yes | Invoice XML document to validate. |
