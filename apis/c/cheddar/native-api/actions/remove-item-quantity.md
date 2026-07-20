# Remove Item Quantity with Cheddar

Decrements a customer item quantity in Cheddar.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/remove-item-quantity/productCode/{productCode}/code/:customerCode/itemCode/:itemCode`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Remove Item Quantity](https://docs.getcheddar.com/#remove-item-quantity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Customer code from Cheddar. |
| `itemCode` | path | `string` | yes | Tracked item code from Cheddar. |
| `quantity` | body | `number` | no | Positive amount to subtract from the current tracked item usage. Defaults to 1.0000 when omitted. |
| `remoteAddress` | body | `string` | no | Client IPv4 address for fraud protection and rate limiting. |
