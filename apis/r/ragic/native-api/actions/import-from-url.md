# Import From URL with Ragic

Imports records into Ragic from a URL.

## Endpoint

- **Method:** `POST`
- **Path:** `/:tabFolderPath/:sheetIndex`
- **Base URL:** `{serverUrl}/mindcloud`
- **Official documentation:** [Import From URL](https://www.ragic.com/docs/api/en/#tag/writing-import)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tabFolderPath` | path | `string` | yes | Folder path segment before the sheet index in the Ragic URL, for example ragic-setup. |
| `sheetIndex` | path | `number` | yes | Numeric sheet identifier from the target Ragic resource URL. |
