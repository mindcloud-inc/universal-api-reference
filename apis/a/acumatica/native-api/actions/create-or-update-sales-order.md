# Create or Update Sales Order with Acumatica

## Endpoint

- **Method:** `PUT`
- **Path:** `/entity/{endpointName}/{endpointVersion}/SalesOrder`
- **Base URL:** `{uRL}`
- **Official documentation:** [Create or Update Sales Order](https://help.acumatica.com/Wiki/ShowWiki.aspx?PageID=91dda8ed-5e92-48a5-a176-9a255506d0d6&wikiname=HelpRoot_Dev_Integration)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | Existing Acumatica entity GUID when updating; leave blank to create. |
| `OrderType` | body | `object` | no | — |
| `OrderType.value` | body | `string` | yes | — |
| `OrderNbr` | body | `object` | no | — |
| `OrderNbr.value` | body | `string` | no | — |
| `CustomerID` | body | `object` | no | — |
| `CustomerID.value` | body | `string` | yes | — |
| `Date` | body | `object` | no | — |
| `Date.value` | body | `date` | no | — |
| `Description` | body | `object` | no | — |
| `Description.value` | body | `string` | no | — |
| `Hold` | body | `object` | no | — |
| `Hold.value` | body | `boolean` | no | — |
| `Details[]` | body | `array<object>` | yes | — |
| `Details[].InventoryID` | body | `object` | no | — |
| `Details[].InventoryID.value` | body | `string` | yes | — |
| `Details[].OrderQty` | body | `object` | no | — |
| `Details[].OrderQty.value` | body | `number` | yes | — |
| `Details[].UOM` | body | `object` | no | — |
| `Details[].UOM.value` | body | `string` | no | — |
| `Details[].WarehouseID` | body | `object` | no | — |
| `Details[].WarehouseID.value` | body | `string` | no | — |
