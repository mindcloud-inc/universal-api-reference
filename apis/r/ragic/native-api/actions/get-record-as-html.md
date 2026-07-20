# Get Record As HTML with Ragic

Retrieves a record as HTML from Ragic.

## Endpoint

- **Method:** `GET`
- **Path:** `/:tabFolderPath/:sheetIndex/:recordId.xhtml`
- **Base URL:** `{serverUrl}/mindcloud`
- **Official documentation:** [Get Record As HTML](https://www.ragic.com/docs/api/en/#tag/reading-exports/operation/getRecordHtml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tabFolderPath` | path | `string` | yes | Folder path segment before the sheet index in the Ragic URL, for example ragic-setup. |
| `sheetIndex` | path | `number` | yes | Numeric sheet identifier from the target Ragic resource URL. |
| `recordId` | path | `number` | yes | Numeric record ID from the target Ragic record URL. |
