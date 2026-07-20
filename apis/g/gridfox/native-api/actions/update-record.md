# Update Record with Gridfox

Updates an existing record in a Gridfox table.

## Endpoint

- **Method:** `PUT`
- **Path:** `/data/:tableName/:referenceFieldValue`
- **Base URL:** `https://api.gridfox.com/`
- **Official documentation:** [Update Record](https://api.gridfox.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `referenceFieldValue` | path | `string` | no | Record reference field value from the path parameter. |
| `tableName` | path | `string` | no | Gridfox table name from the path parameter. |
