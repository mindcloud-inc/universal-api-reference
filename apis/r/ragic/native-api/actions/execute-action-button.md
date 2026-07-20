# Execute Action Button with Ragic

Executes an action button on a Ragic record.

## Endpoint

- **Method:** `POST`
- **Path:** `/:tabFolderPath/:sheetIndex/:recordId`
- **Base URL:** `{serverUrl}/mindcloud`
- **Official documentation:** [Execute Action Button](https://www.ragic.com/docs/api/en/#tag/writing-action)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tabFolderPath` | path | `string` | yes | The folder path from the Ragic URL, for example `ragic-setup`. |
| `sheetIndex` | path | `number` | yes | The sheet number from the Ragic URL. |
| `recordId` | path | `number` | yes | The record ID from the Ragic record URL. |
| `bId` | query | `number` | yes | The action-button ID returned by `List Action Buttons`. |
