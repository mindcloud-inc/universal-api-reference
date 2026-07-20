# Mass Unlock Records with Ragic

Unlocks multiple records in Ragic.

## Endpoint

- **Method:** `POST`
- **Path:** `/:tabFolderPath/:sheetIndex/massOperation/massLock`
- **Base URL:** `{serverUrl}/mindcloud`
- **Official documentation:** [Mass Unlock Records](https://www.ragic.com/docs/api/en/#tag/mass-operations/Mass-Lock)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tabFolderPath` | path | `string` | yes | Folder path segment before the sheet index in the Ragic URL, for example ragic-setup. |
| `sheetIndex` | path | `number` | yes | Numeric sheet identifier from the target Ragic resource URL. |
| `recordId` | query | `number` | no | Single Ragic record ID to target for the mass operation when you are not using a where filter. |
| `where` | query | `string` | no | Optional Ragic where clause in the documented `<fieldId>,<operand>,<value>` format for targeting multiple records. |
