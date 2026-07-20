# Update Data Table Row with Revel Digital

## Endpoint

- **Method:** `PUT`
- **Path:** `/datatables/:tableId/rows/:rowId`
- **Base URL:** `https://api.reveldigital.com`
- **Official documentation:** [Update Data Table Row](https://developer.reveldigital.com/rest-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `rowId` | path | `string` | yes | Unique identifier of the data table row. |
| `tableId` | path | `string` | yes | Unique identifier of the data table. |
