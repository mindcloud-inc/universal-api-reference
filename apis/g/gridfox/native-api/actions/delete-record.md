# Delete Record with Gridfox

Deletes an existing record from a Gridfox table.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/data/:tableName/:referenceFieldValue`
- **Base URL:** `https://api.gridfox.com/`
- **Official documentation:** [Delete Record](https://api.gridfox.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `referenceFieldValue` | path | `string` | no | Record reference field value from the path parameter. |
| `tableName` | path | `string` | no | Gridfox table name from the path parameter. |
