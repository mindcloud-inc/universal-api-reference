# List Record Audits with Gridfox

Retrieves audit entries for a Gridfox record.

## Endpoint

- **Method:** `GET`
- **Path:** `/data/:tableName/:referenceFieldValue/audit`
- **Base URL:** `https://api.gridfox.com/`
- **Official documentation:** [List Record Audits](https://api.gridfox.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `referenceFieldValue` | path | `string` | no | Record reference field value from the path parameter. |
| `tableName` | path | `string` | no | Gridfox table name from the path parameter. |
