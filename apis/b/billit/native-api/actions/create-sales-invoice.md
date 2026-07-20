# Create Sales Invoice with Billit

Creates a sales invoice in Billit.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/orders`
- **Base URL:** `https://api.sandbox.billit.be`
- **Official documentation:** [Create Sales Invoice](https://docs.billit.be/reference/order_postorders-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `OrderNumber` | body | `string` | yes | Unique invoice number from your source system. |
| `OrderDate` | body | `date` | yes | Invoice issue date in YYYY-MM-DD format. |
| `DeliveryDate` | body | `date` | no | Delivery date in YYYY-MM-DD format. |
| `ExpiryDate` | body | `date` | yes | Invoice due date in YYYY-MM-DD format. |
| `Customer` | body | `object` | yes | Billit customer object; include Name, PartyType, VATNumber or address details as needed. |
| `OrderLines[]` | body | `array<object>` | yes | Array of Billit order line objects. |
| `Reference` | body | `string` | no | Optional buyer purchase-order reference. |
| `Currency` | body | `string` | no | Optional ISO currency code; Billit defaults to EUR when omitted. |
