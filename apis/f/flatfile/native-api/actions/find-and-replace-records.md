# Find And Replace Records with Flatfile

Finds and replaces matching record values in Flatfile.

## Endpoint

- **Method:** `PUT`
- **Path:** `/sheets/:sheetId/find-replace`
- **Base URL:** `https://api.x.flatfile.com/v1`
- **Official documentation:** [Find And Replace Records](https://reference.flatfile.com/api-reference/records/find-and-replace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fieldKey` | body | `string` | yes | Field key to search and replace. |
| `sheetId` | path | `string` | yes | Flatfile sheet identifier. |
