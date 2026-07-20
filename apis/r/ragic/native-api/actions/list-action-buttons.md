# List Action Buttons with Ragic

Retrieves action buttons from Ragic.

## Endpoint

- **Method:** `GET`
- **Path:** `/:tabFolderPath/:sheetIndex/metadata/actionButton`
- **Base URL:** `{serverUrl}/mindcloud`
- **Official documentation:** [List Action Buttons](https://www.ragic.com/docs/api/en/#tag/writing-action)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tabFolderPath` | path | `string` | yes | The folder path from the Ragic URL, for example `ragic-setup`. |
| `sheetIndex` | path | `number` | yes | The sheet number from the Ragic URL. |
| `category` | query | `string` | no | The action-button category. Ragic documents `massOperation` for this listing endpoint. |
