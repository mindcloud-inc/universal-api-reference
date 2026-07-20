# List Pack Types (SEARCH) with Logiwa Legacy WMS

By using these endpoints, the users can obtain all the information that is related to the pack types of the items.

To obtain this information, the users should first reach the Pack Type ID values by using the InventoryItemPackTypeSearch endpoint. After this process, the users will be able to use the InventoryItemPackTypeGet endpoint.

## Endpoint

- **Method:** `POST`
- **Path:** `/en/api/IntegrationApi/InventoryItemPackTypeSearch`
- **Base URL:** `https://{uRL}.logiwa.com/`
- **Official documentation:** [List Pack Types (SEARCH)](https://developer.logiwa.com/?id=5e71514fe6466c0c70d9c50a)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `InventoryItemID` | body | `string` | no |
