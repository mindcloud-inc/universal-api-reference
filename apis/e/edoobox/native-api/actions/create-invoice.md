# Create Invoice with Edoobox

Creates a new invoice in Edoobox.

## Endpoint

- **Method:** `POST`
- **Path:** `/invoice`
- **Base URL:** `https://app2.edoobox.com/v2`
- **Official documentation:** [Create Invoice](https://api.docs.edoobox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transaction` | body | `string` | yes | edoobox transaction ID to invoice. |
