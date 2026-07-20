# Validate Italy Invoice with Invoice.xhub

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/invoice/IT/validate`
- **Base URL:** `https://service.invoice-api.xhub.io`
- **Official documentation:** [Validate Italy Invoice](https://invoice-api.xhub.io/en/docs/api/validator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `xml` | body | `string` | yes | Invoice XML document to validate. |
