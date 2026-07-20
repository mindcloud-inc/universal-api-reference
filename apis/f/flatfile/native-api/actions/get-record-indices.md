# Get Record Indices with Flatfile

Retrieves record indices from a Flatfile sheet.

## Endpoint

- **Method:** `GET`
- **Path:** `/sheets/:sheetId/records/indices`
- **Base URL:** `https://api.x.flatfile.com/v1`
- **Official documentation:** [Get Record Indices](https://reference.flatfile.com/api-reference/records/indices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | yes | Comma-delimited record IDs to inspect. |
| `sheetId` | path | `string` | yes | Flatfile sheet ID. |
