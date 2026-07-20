# Mass Execute Action Button with Ragic

Executes an action button on multiple Ragic records.

## Endpoint

- **Method:** `POST`
- **Path:** `/:tabFolderPath/:sheetIndex/massOperation/massActionButton`
- **Base URL:** `{serverUrl}/mindcloud`
- **Official documentation:** [Mass Execute Action Button](https://www.ragic.com/docs/api/en/#tag/mass-operations/Mass-Action-Button)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tabFolderPath` | path | `string` | yes | Folder path segment before the sheet index in the Ragic URL, for example ragic-setup. |
| `sheetIndex` | path | `number` | yes | Numeric sheet identifier from the target Ragic resource URL. |
| `recordId` | query | `number` | no | Single Ragic record ID to target for the mass operation when you are not using a where filter. |
| `where` | query | `string` | no | Optional Ragic where clause in the documented `<fieldId>,<operand>,<value>` format for targeting multiple records. |
| `buttonId` | body | `string` | yes | Mass-operation action-button ID from the Ragic metadata/actionButton endpoint. |
