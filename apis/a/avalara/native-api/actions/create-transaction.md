# Create Transaction with Avalara AvaTax

## Endpoint

- **Method:** `POST`
- **Path:** `transactions/create`
- **Base URL:** `{environment}`
- **Official documentation:** [Create Transaction](https://developer.avalara.com/api-reference/avatax/rest/v2/methods/Transactions/CreateTransaction/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addresses.pointOfOrderOrigin.line1` | body | `string` | no | — |
| `addresses.shipFrom` | body | `object` | no | — |
| `addresses.shipFrom.line1` | body | `string` | no | — |
| `addresses.shipTo.line1` | body | `string` | no | — |
| `lines[]` | body | `array` | yes | — |
| `lines[].number` | body | `string` | no | — |
| `addresses.pointOfOrderOrigin.city` | body | `string` | no | — |
| `addresses.shipFrom.city` | body | `string` | no | — |
| `addresses.shipTo` | body | `object` | no | — |
| `addresses.shipTo.city` | body | `string` | no | — |
| `lines[].quantity` | body | `number` | no | — |
| `addresses.pointOfOrderOrigin` | body | `object` | no | — |
| `addresses.pointOfOrderOrigin.region` | body | `string` | no | — |
| `addresses.shipFrom.region` | body | `string` | no | — |
| `addresses.shipTo.region` | body | `string` | no | — |
| `lines[].amount` | body | `number` | yes | — |
| `addresses.pointOfOrderOrigin.country` | body | `string` | no | — |
| `addresses.shipFrom.country` | body | `string` | no | — |
| `addresses.shipTo.country` | body | `string` | no | — |
| `lines[].taxCode` | body | `string` | no | — |
| `addresses.pointOfOrderOrigin.postalCode` | body | `string` | no | — |
| `addresses.shipFrom.postalCode` | body | `string` | no | — |
| `addresses.shipTo.postalCode` | body | `string` | no | — |
| `lines[].itemCode` | body | `string` | no | — |
| `addresses.shipFrom.line2` | body | `string` | no | — |
| `addresses.shipTo.line2` | body | `string` | no | — |
| `lines[].description` | body | `string` | no | — |
| `referenceCode` | body | `string` | no | — |
| `reportingLocationCode` | body | `string` | no | — |
| `code` | body | `string` | no | — |
| `$include` | query | `string` | no | Comma-separated related objects to include in the response. |
| `addresses` | body | `object` | no | — |
| `commit` | body | `boolean` | no | Format: `toggle`. |
| `companyCode` | body | `string` | no | — |
| `currencyCode` | body | `string` | no | — |
| `customerCode` | body | `string` | yes | — |
| `date` | body | `date` | yes | — |
| `description` | body | `string` | no | — |
| `purchaseOrderNo` | body | `string` | no | — |
| `type` | body | `string` | no | — |
