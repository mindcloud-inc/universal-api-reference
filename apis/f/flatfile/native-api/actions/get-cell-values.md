# Get Cell Values with Flatfile

Retrieves record cell values by field in Flatfile.

## Endpoint

- **Method:** `GET`
- **Path:** `/sheets/:sheetId/cells`
- **Base URL:** `https://api.x.flatfile.com/v1`
- **Official documentation:** [Get Cell Values](https://reference.flatfile.com/api-reference/sheets/get-cell-values)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `distinct` | query | `string` | yes | Must be true to request distinct cell values. |
| `sheetId` | path | `string` | yes | Flatfile sheet ID. |
