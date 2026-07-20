# Upload Workbook with Microsoft 365 Excel

Uploads a workbook file to Microsoft 365 Excel.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1.0/drives/:driveId/items/:parentFolderId:/:fileName:/content`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Upload Workbook](https://learn.microsoft.com/en-us/graph/api/driveitem-put-content?view=graph-rest-1.0)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveId` | path | `string` | yes | Drive ID for the destination drive. For a folder or file returned by Graph, use `parentReference.driveId`. |
| `parentFolderId` | path | `string` | yes | Drive item ID of the destination folder. From the prior output shown, this is `parentReference.id`, not the workbook file `id`. |
| `fileName` | path | `string` | yes | Workbook filename to create, including the `.xlsx` extension. |
| `workbookFile` | body | `string` | yes | Base64-encoded contents of a valid .xlsx workbook file. The action decodes this value and sends the raw workbook bytes to Microsoft Graph. |
