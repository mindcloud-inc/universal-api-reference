# Mass Reject Records with Ragic

Rejects multiple records in Ragic.

## Endpoint

- **Method:** `POST`
- **Path:** `/:tabFolderPath/:sheetIndex/massOperation/massApproval`
- **Base URL:** `{serverUrl}/mindcloud`
- **Official documentation:** [Mass Reject Records](https://www.ragic.com/docs/api/en/#tag/mass-operations/Mass-Approval)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tabFolderPath` | path | `string` | yes | Folder path segment before the sheet index in the Ragic URL, for example ragic-setup. |
| `sheetIndex` | path | `number` | yes | Numeric sheet identifier from the target Ragic resource URL. |
| `recordId` | query | `number` | no | Single Ragic record ID to target for the mass operation when you are not using a where filter. |
| `where` | query | `string` | no | Optional Ragic where clause in the documented `<fieldId>,<operand>,<value>` format for targeting multiple records. |
| `comment` | body | `string` | no | Optional comment that accompanies the rejection action. |
