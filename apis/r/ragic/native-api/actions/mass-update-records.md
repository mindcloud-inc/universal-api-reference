# Mass Update Records with Ragic

Updates multiple records in Ragic.

## Endpoint

- **Method:** `POST`
- **Path:** `/:tabFolderPath/:sheetIndex/massOperation/massUpdate`
- **Base URL:** `{serverUrl}/mindcloud`
- **Official documentation:** [Mass Update Records](https://www.ragic.com/docs/api/en/#tag/mass-operations/Mass-Update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tabFolderPath` | path | `string` | yes | Folder path segment before the sheet index in the Ragic URL, for example ragic-setup. |
| `sheetIndex` | path | `number` | yes | Numeric sheet identifier from the target Ragic resource URL. |
| `recordId` | query | `number` | no | Single Ragic record ID to target for the mass operation when you are not using a where filter. |
| `where` | query | `string` | no | Optional Ragic where clause in the documented `<fieldId>,<operand>,<value>` format for targeting multiple records. |
| `action[0].field` | body | `number` | yes | Field ID to update on every selected record. |
| `action[0].value` | body | `string` | yes | New field value to write to the selected records. |
