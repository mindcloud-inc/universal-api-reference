# List Product Clients with Megaventory

Retrieves product client links from Megaventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/ProductClientGet`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [List Product Clients](https://api.megaventory.com/v2017a/json/metadata?op=ProductClientGet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filters` | body | `list<object>` | no | Megaventory filter rule objects. |
| `ReturnTopNRecords` | body | `number` | no | Maximum number of rows Megaventory should return. |
