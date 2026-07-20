# Set Item Quantity with Cheddar

Sets a customer item quantity in Cheddar.

## Endpoint

- **Method:** `POST`
- **Path:** `/customers/set-item-quantity/productCode/{productCode}/code/:customerCode/itemCode/:itemCode`
- **Base URL:** `https://getcheddar.com/xml`
- **Official documentation:** [Set Item Quantity](https://docs.getcheddar.com/#set-item-quantity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Customer code from Cheddar. |
| `itemCode` | path | `string` | yes | Tracked item code from Cheddar. |
| `quantity` | body | `number` | yes | Exact tracked item quantity to set. |
| `invoicePeriod` | body | `string` | no | Billing period: current (default) or outstanding. |
| `remoteAddress` | body | `string` | no | Client IPv4 address for fraud protection and rate limiting. |
