# Insert Purchase Order with Logiwa Legacy WMS

By using this endpoint, the users can create single or multiple purchase orders with lines.

All the products used should be defined in the system before creating any purchase orders.

## Endpoint

- **Method:** `POST`
- **Path:** `en/api/IntegrationApi/PurchaseOrderBulkInsert`
- **Base URL:** `https://{uRL}.logiwa.com/`
- **Official documentation:** [Insert Purchase Order](https://developer.logiwa.com/?id=5df0dc03e6466c2eec992f5f)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Details[].ItemCode` | body | `string` | no | — |
| `Details[].ItemPackType` | body | `string` | no | — |
| `Details[].Quantity` | body | `number` | no | — |
| `Details[].LineCode` | body | `string` | no | — |
| `Details[].TotalLinePrice` | body | `number` | no | Total purchase price of the order line |
| `Details[].Note` | body | `string` | no | — |
| `AddressText` | body | `string` | no | — |
| `City` | body | `string` | no | — |
| `ClientreferenceCode` | body | `string` | no | — |
| `Code` | body | `string` | no | — |
| `Country` | body | `string` | no | — |
| `Depositor` | body | `string` | yes | — |
| `Details[]` | body | `array<object>` | no | — |
| `Email` | body | `string` | no | — |
| `GeoCode` | body | `string` | no | — |
| `InventorySite` | body | `string` | yes | — |
| `Notes` | body | `string` | no | — |
| `PartyAddressType` | body | `string` | no | — |
| `PurchaseOrderStatus` | body | `string` | no | — |
| `PurchaseOrderType` | body | `string` | no | — |
| `State` | body | `string` | no | — |
| `Supplier` | body | `string` | no | — |
| `SupplierAddress` | body | `string` | no | — |
