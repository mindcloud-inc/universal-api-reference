# Delete Table with Docsumo

Deletes one or more Docsumo database tables.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/raichu/drop_down/db/delete/`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [Delete Table](https://support.docsumo.com/reference/delete-table)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ddid` | body | `string` | no | Database table ID to delete. |
