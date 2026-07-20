# Delete Field File with Gridfox

Deletes a file from a Gridfox record field.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/data/:tableName/:referenceFieldValue/:fieldName/:fileName`
- **Base URL:** `https://api.gridfox.com/`
- **Official documentation:** [Delete Field File](https://api.gridfox.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fieldName` | path | `string` | no | Gridfox file field name from the path parameter. |
| `fileName` | path | `string` | no | File name from the path parameter. |
| `referenceFieldValue` | path | `string` | no | Record reference field value from the path parameter. |
| `tableName` | path | `string` | no | Gridfox table name from the path parameter. |
