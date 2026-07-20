# List Inventory Locations with Megaventory

Retrieves inventory location records from Megaventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/InventoryLocationGet`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [List Inventory Locations](https://api.megaventory.com/v2017a/json/metadata?op=InventoryLocationGet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filters` | body | `list<object>` | no | Megaventory filter rule objects. |
| `ReturnTopNRecords` | body | `number` | no | Maximum number of rows Megaventory should return. |
| `showDeleted` | body | `boolean` | no | Include archived inventory locations. |
| `IncludeTransit` | body | `boolean` | no | Include transit inventory locations. |
