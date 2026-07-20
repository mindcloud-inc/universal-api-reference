# Validate Czech Republic Invoice with Invoice.xhub

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/invoice/CZ/validate`
- **Base URL:** `https://service.invoice-api.xhub.io`
- **Official documentation:** [Validate Czech Republic Invoice](https://invoice-api.xhub.io/en/docs/api/validator)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `xml` | body | `string` | yes | XML invoice payload to validate. |
