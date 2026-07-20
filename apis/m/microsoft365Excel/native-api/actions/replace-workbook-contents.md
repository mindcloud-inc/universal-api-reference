# Replace Workbook Contents with Microsoft 365 Excel

Replaces workbook file contents in Microsoft 365 Excel.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1.0/drives/:driveId/items/:driveItemId/content`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Replace Workbook Contents](https://learn.microsoft.com/en-us/graph/api/driveitem-put-content?view=graph-rest-1.0)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveId` | path | `string` | yes | Drive ID containing the workbook item. From Graph file output, use `parentReference.driveId`. |
| `driveItemId` | path | `string` | yes | Drive item ID of the workbook file to replace. From the output shown, this is the top-level `id`. |
| `workbookFile` | body | `string` | yes | Base64-encoded contents of a valid .xlsx workbook file. The action decodes this value and sends the raw workbook bytes to Microsoft Graph. |
