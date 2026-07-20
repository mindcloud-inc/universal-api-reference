# List Records with Ragic

Retrieves records from Ragic.

## Endpoint

- **Method:** `GET`
- **Path:** `/:tabFolderPath/:sheetIndex`
- **Base URL:** `{serverUrl}/mindcloud`
- **Official documentation:** [List Records](https://www.ragic.com/docs/api/en/#tag/reading-format/operation/listRecords)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tabFolderPath` | path | `string` | yes | Folder path segment before the sheet index in the Ragic URL, for example mindcloud. |
| `sheetIndex` | path | `number` | yes | Numeric sheet identifier from the target Ragic resource URL. |
