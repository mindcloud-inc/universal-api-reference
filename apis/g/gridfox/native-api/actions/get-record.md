# Get Record with Gridfox

Retrieves a record from a Gridfox table.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/:tableName/:referenceFieldValue`
- **Base URL:** `https://api.gridfox.com/`
- **Official documentation:** [Get Record](https://api.gridfox.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `referenceFieldValue` | path | `string` | no | Record reference field value from the path parameter. |
| `tableName` | path | `string` | no | Gridfox table name from the path parameter. |
