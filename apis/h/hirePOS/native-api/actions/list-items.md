# List Items with HirePOS

Finds items in HirePOS by item search fields.

## Endpoint

- **Method:** `GET`
- **Path:** `/Items`
- **Base URL:** `https://api.hirepos.com`
- **Official documentation:** [List Items](https://docs.hirepos.com/en/articles/3084097)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Code` | query | `string` | no | Find an item by its HirePOS item code. |
| `Barcode` | query | `string` | no | Find an item by barcode. |
| `SupplierCode` | query | `string` | no | Find an item by supplier code. |
| `Serial` | query | `string` | no | Find an item by serial tracking number. |
