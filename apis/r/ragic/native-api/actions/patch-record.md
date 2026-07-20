# Patch Record with Ragic

Partially updates an existing record in Ragic.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:tabFolderPath/:sheetIndex/:recordId`
- **Base URL:** `{serverUrl}/mindcloud`
- **Official documentation:** [Patch Record](https://www.ragic.com/docs/api/en/#tag/writing-modify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tabFolderPath` | path | `string` | yes | The folder path from the Ragic URL, for example `ragic-setup`. |
| `sheetIndex` | path | `number` | yes | The sheet number from the Ragic URL. |
| `recordId` | path | `number` | yes | The record ID from the Ragic record URL. |
| `doFormula` | body | `boolean` | no | Recalculate formulas before saving. |
| `doDefaultValue` | body | `boolean` | no | Load default values when updating the record. |
| `doLinkLoad` | body | `string` | no | Run Ragic link-and-load logic. Use `true` or `first`. |
| `doWorkflow` | body | `boolean` | no | Execute the workflow script associated with this update. |
| `notification` | body | `boolean` | no | Send notifications to relevant users. |
| `checkLock` | body | `boolean` | no | Check whether the record is locked before updating. |
