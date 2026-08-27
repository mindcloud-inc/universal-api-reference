# Send Inventory Quantity(to Custom Field) with Acumatica

## Endpoint

- **Method:** `PUT`
- **Path:** `/entity/{endpointName}/{endpointVersion}/ItemWarehouse`
- **Base URL:** `{uRL}`
- **Official documentation:** [Send Inventory Quantity(to Custom Field)](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `UsrLogSyncDateTime.value` | body | `string` | no |
| `InventoryID.value` | body | `string` | no |
| `UsrLogQOH` | body | `object` | no |
| `UsrLogQOH.value` | body | `number` | no |
| `WarehouseID.value` | body | `string` | no |
| `InventoryID` | body | `object` | no |
| `WarehouseID` | body | `object` | no |
| `UsrLogSyncDateTime` | body | `object` | no |
