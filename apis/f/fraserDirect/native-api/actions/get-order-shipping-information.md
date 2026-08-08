# Get order shipping information with Fraser Direct

## Endpoint

- **Method:** `GET`
- **Path:** `/GetOrderShippingInformation`
- **Base URL:** `{baseURL}`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `OrderNumber` | body | `string` | no | Provide OrderNumber, PO, or both. |
| `PO` | body | `string` | no | Provide OrderNumber, PO, or both. If both are provided, they must match the same order. |
