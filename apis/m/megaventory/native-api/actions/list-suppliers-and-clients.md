# List Suppliers and Clients with Megaventory

Retrieves supplier and client records from Megaventory.

## Endpoint

- **Method:** `POST`
- **Path:** `/json/reply/SupplierClientGet`
- **Base URL:** `https://api.megaventory.com/v2017a`
- **Official documentation:** [List Suppliers and Clients](https://api.megaventory.com/v2017a/json/metadata?op=SupplierClientGet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Filters` | body | `list<object>` | no | Megaventory filter rule objects. |
| `ReturnTopNRecords` | body | `number` | no | Maximum number of rows Megaventory should return. |
| `showDeleted` | body | `boolean` | no | Include archived supplier or client records. |
