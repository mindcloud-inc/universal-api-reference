# Bulk Update Records with Flatfile

Bulk updates matching records in a Flatfile sheet.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/sheets/:sheetId/records/bulk-update`
- **Base URL:** `https://api.x.flatfile.com/v1`
- **Official documentation:** [Bulk Update Records](https://reference.flatfile.com/api-reference/records/bulk-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fieldUpdates` | body | `string` | yes | Field updates payload. |
| `sheetId` | path | `string` | yes | Flatfile sheet identifier. |
