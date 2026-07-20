# Delete Record with Ragic

Deletes an existing record from Ragic.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/:tabFolderPath/:sheetIndex/:recordId`
- **Base URL:** `{serverUrl}/mindcloud`
- **Official documentation:** [Delete Record](https://www.ragic.com/docs/api/en/#tag/writing-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tabFolderPath` | path | `string` | yes | The folder path from the Ragic URL, for example `ragic-setup`. |
| `sheetIndex` | path | `number` | yes | The sheet number from the Ragic URL. |
| `recordId` | path | `number` | yes | The record ID from the Ragic record URL. |
