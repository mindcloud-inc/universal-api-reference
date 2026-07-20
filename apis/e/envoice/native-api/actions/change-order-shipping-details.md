# Change Order Shipping Details with Envoice

Updates order shipping details in Envoice.

## Endpoint

- **Method:** `POST`
- **Path:** `order/changeshippingdetails`
- **Base URL:** `https://www.envoice.in/api`
- **Official documentation:** [Change Order Shipping Details](https://www.envoice.in/reference/api/docs/v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Address` | body | `string` | no | Shipping street address. |
| `CountryId` | body | `number` | yes | Shipping country identifier. |
| `Email` | body | `string` | yes | Shipping recipient email. |
| `Name` | body | `string` | yes | Shipping recipient name. |
| `orderId` | query | `number` | yes | Order identifier whose shipping details should change. |
| `PhoneNumber` | body | `string` | no | Shipping phone number. |
