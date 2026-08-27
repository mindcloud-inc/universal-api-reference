# Inventory Adjustment with Acumatica

## Endpoint

- **Method:** `PUT`
- **Path:** `/entity/{endpointName}/{endpointVersion}/InventoryAdjustment`
- **Base URL:** `{uRL}`
- **Official documentation:** [Inventory Adjustment](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `Branch.value` | body | `string` | no |
| `BranchID.value` | body | `string` | no |
| `Date.value` | body | `string` | no |
| `Description.value` | body | `string` | no |
| `Details[].expirationDate.value` | body | `string` | no |
| `Details[].InventoryID` | body | `object` | no |
| `Details[].InventoryID.value` | body | `string` | no |
| `Details[].LocationID.value` | body | `string` | no |
| `Details[].LotSerialNbr.value` | body | `string` | no |
| `Details[].Qty.value` | body | `number` | no |
| `Details[].ReasonCode.value` | body | `string` | no |
| `Details[].UOM.value` | body | `string` | no |
| `Details[].UsrLogTranID.value` | body | `string` | no |
| `Details[].WarehouseID.value` | body | `string` | no |
| `ExternalRef.value` | body | `string` | no |
| `ReferenceNbr` | body | `object` | no |
| `ReferenceNbr.value` | body | `string` | no |
| `UsrLogAdjustment.value` | body | `boolean` | no |
| `Date` | body | `object` | no |
| `Details[].WarehouseID` | body | `object` | no |
| `Details[].LocationID` | body | `object` | no |
| `ExternalRef` | body | `object` | no |
| `Description` | body | `object` | no |
| `Details[].Qty` | body | `object` | no |
| `Branch` | body | `object` | no |
| `Details[].UOM` | body | `object` | no |
| `Details[]` | body | `array` | no |
| `Details[].LotSerialNbr` | body | `object` | no |
| `Details[].ReasonCode` | body | `object` | no |
| `UsrLogAdjustment` | body | `object` | no |
| `BranchID` | body | `object` | no |
| `Details[].expirationDate` | body | `object` | no |
| `Details[].UsrLogTranID` | body | `object` | no |
