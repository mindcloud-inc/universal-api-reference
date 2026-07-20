# Import Excel Workbook in Workspace with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `groups/[:groupId]/imports`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Import Excel Workbook in Workspace](https://learn.microsoft.com/en-us/rest/api/power-bi/imports/post-import-in-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | Power BI workspace ID that will receive the imported Excel workbook. |
| `filePath` | body | `string` | yes | OneDrive for Business path to the Excel .xlsx workbook to import. |
| `connectionType` | body | `list` | no | Optional. Power BI import connection type for a OneDrive for Business Excel file. Accepted values: `0`, `1`. |
| `nameConflict` | query | `list` | no | Optional. Conflict handling mode for an import with the same name. Power BI defaults to Ignore. Accepted values: `0`, `1`, `2`, `3`, `4`. |
