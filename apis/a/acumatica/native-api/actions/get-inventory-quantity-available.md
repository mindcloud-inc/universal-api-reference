# Get Inventory Quantity Available with Acumatica

## Endpoint

- **Method:** `PUT`
- **Path:** `/entity/{endpointName}/{endpointVersion}/InventoryQuantityAvailable`
- **Base URL:** `{uRL}`
- **Official documentation:** [Get Inventory Quantity Available](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `inventoryID.value` | body | `string` | no |
| `lastModifiedDateTime.value` | body | `string` | no |
| `inventoryID` | body | `object` | no |
| `lastModifiedDateTime` | body | `object` | no |
