# Upload Field Files with Gridfox

Adds files to a file field in Gridfox.

## Endpoint

- **Method:** `POST`
- **Path:** `/data/:tableName/:referenceFieldValue/:fieldName`
- **Base URL:** `https://api.gridfox.com/`
- **Official documentation:** [Upload Field Files](https://api.gridfox.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fieldName` | path | `string` | no | Gridfox file field name from the path parameter. |
| `referenceFieldValue` | path | `string` | no | Record reference field value from the path parameter. |
| `tableName` | path | `string` | no | Gridfox table name from the path parameter. |
