# Lock Record with Ragic

Locks a record in Ragic.

## Endpoint

- **Method:** `POST`
- **Path:** `/:tabFolderPath/:sheetIndex/:recordId`
- **Base URL:** `{serverUrl}/mindcloud`
- **Official documentation:** [Lock Record](https://www.ragic.com/docs/api/en/#tag/writing-lock)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tabFolderPath` | path | `string` | yes | The folder path from the Ragic URL, for example `ragic-setup`. |
| `sheetIndex` | path | `number` | yes | The sheet number from the Ragic URL. |
| `recordId` | path | `number` | yes | The record ID from the Ragic record URL. |
