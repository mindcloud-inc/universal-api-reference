# Upload Files and Images with Ragic

Uploads files and images to Ragic.

## Endpoint

- **Method:** `POST`
- **Path:** `/:tabFolderPath/:sheetIndex`
- **Base URL:** `{serverUrl}/mindcloud`
- **Official documentation:** [Upload Files and Images](https://www.ragic.com/docs/api/en/#tag/writing-upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tabFolderPath` | path | `string` | yes | Folder path segment before the sheet index in the Ragic URL, for example ragic-setup. |
| `sheetIndex` | path | `number` | yes | Numeric sheet identifier from the target Ragic resource URL. |
