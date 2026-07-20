# Delete Records with Flatfile

Deletes records from a Flatfile sheet.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/sheets/:sheetId/records`
- **Base URL:** `https://api.x.flatfile.com/v1`
- **Official documentation:** [Delete Records](https://reference.flatfile.com/api-reference/records/delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | yes | Comma-delimited record IDs to delete. |
| `sheetId` | path | `string` | yes | Flatfile sheet ID. |
