# Add Item Quantity with Cheddar

Increments a customer item quantity in Cheddar.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/add-item-quantity/productCode/{productCode}/code/:customerCode/itemCode/:itemCode`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Add Item Quantity](https://docs.getcheddar.com/#add-item-quantity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Customer code from Cheddar. |
| `itemCode` | path | `string` | yes | Tracked item code from Cheddar. |
| `quantity` | body | `number` | no | Positive amount to add to the current tracked item usage. Defaults to 1.0000 when omitted. |
| `remoteAddress` | body | `string` | no | Client IPv4 address for fraud protection and rate limiting. |
