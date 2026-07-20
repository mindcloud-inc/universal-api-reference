# Create Record with Ragic

Creates a new record in Ragic.

## Endpoint

- **Method:** `POST`
- **Path:** `/:tabFolderPath/:sheetIndex`
- **Base URL:** `{serverUrl}/mindcloud`
- **Official documentation:** [Create Record](https://www.ragic.com/docs/api/en/#tag/writing-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tabFolderPath` | path | `string` | yes | Folder path segment before the sheet index in the Ragic URL, for example ragic-setup. |
| `sheetIndex` | path | `number` | yes | Numeric sheet identifier from the target Ragic resource URL. |
| `doFormula` | body | `boolean` | no | Recalculate formulas before create. When true, workflow scripts will not run. |
| `doDefaultValue` | body | `boolean` | no | Load default values when creating the record. |
| `doLinkLoad` | body | `string` | no | Execute link/load operations. Use true to run after formulas or first to run before formulas. |
| `doWorkflow` | body | `boolean` | no | Execute the workflow script associated with the sheet. |
| `notification` | body | `boolean` | no | Send notifications to relevant users. Ragic defaults this to true when omitted. |
