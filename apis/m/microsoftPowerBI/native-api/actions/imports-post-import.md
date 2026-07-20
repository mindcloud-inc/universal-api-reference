# Post Import with Microsoft Power BI

## Endpoint

- **Method:** `POST`
- **Path:** `imports`
- **Base URL:** `https://api.powerbi.com/v1.0/myorg`
- **Official documentation:** [Post Import](https://learn.microsoft.com/en-us/rest/api/power-bi/imports/post-import)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `datasetDisplayName` | query | `string` | yes | The display name of the dataset, should include file extension. Not supported when importing from OneDrive for Business. |
| `nameConflict` | query | `object` | no | Specifies what to do if a dataset with the same name already exists. The default value is Ignore. For RDL files, Abort and Overwrite are the only supported options and not others. |
| `overrideModelLabel` | query | `boolean` | no | Whether to override the existing label on a model when republishing a Power BI .pbix file. The service default value is true. |
| `overrideReportLabel` | query | `boolean` | no | Whether to override the existing report label when republishing a Power BI .pbix file. The service default value is true. |
| `skipReport` | query | `boolean` | no | Whether to skip report import. If specified, the value must be true. Only supported for Power BI .pbix files. |
| `subfolderObjectId` | query | `string` | no | The subfolder ID to import the file to subfolder. |
| `connectionType` | body | `object` | no | The import connection type for a OneDrive for Business file |
| `filePath` | body | `string` | no | The path of the OneDrive for Business Excel (.xlsx) file to import, which can be absolute or relative. Power BI .pbix files aren't supported. |
| `fileUrl` | body | `string` | no | The shared access signature URL of the temporary blob storage used to import large Power BI .pbix files between 1 GB and 10 GB in size. |
