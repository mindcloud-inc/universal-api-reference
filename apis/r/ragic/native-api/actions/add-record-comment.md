# Add Record Comment with Ragic

Adds a comment to a record in Ragic.

## Endpoint

- **Method:** `POST`
- **Path:** `/:tabFolderPath/:sheetIndex/:recordId`
- **Base URL:** `{serverUrl}/mindcloud`
- **Official documentation:** [Add Record Comment](https://www.ragic.com/docs/api/en/#tag/writing-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tabFolderPath` | path | `string` | yes | The folder path from the Ragic URL, for example `ragic-setup`. |
| `sheetIndex` | path | `number` | yes | The sheet number from the Ragic URL. |
| `recordId` | path | `number` | yes | The record ID from the Ragic record URL. |
| `c` | body | `string` | yes | The comment text to add to the record. |
| `at` | body | `string` | no | Optional attachment file to upload with the comment. |
