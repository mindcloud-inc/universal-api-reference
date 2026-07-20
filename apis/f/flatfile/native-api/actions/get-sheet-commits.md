# Get Sheet Commits with Flatfile

Retrieves commit versions for a sheet in Flatfile.

## Endpoint

- **Method:** `GET`
- **Path:** `/sheets/:sheetId/commits`
- **Base URL:** `https://api.x.flatfile.com/v1`
- **Official documentation:** [Get Sheet Commits](https://reference.flatfile.com/api-reference/sheets/get-sheet-commits)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sheetId` | path | `string` | yes | Flatfile sheet ID. |
