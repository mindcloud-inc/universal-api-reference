# List Sheets with Flatfile

Retrieves a list of sheets from Flatfile.

## Endpoint

- **Method:** `GET`
- **Path:** `/sheets`
- **Base URL:** `https://api.x.flatfile.com/v1`
- **Official documentation:** [List Sheets](https://reference.flatfile.com/api-reference/sheets/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workbookId` | query | `string` | yes | Flatfile workbook ID to list sheets for. |
