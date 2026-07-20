# Create Workbook Session with Microsoft 365 Excel

Creates a workbook session in Microsoft 365 Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/drives/:driveId/items/:driveItemId/workbook/createSession`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Create Workbook Session](https://learn.microsoft.com/en-us/graph/api/workbook-createsession?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driveId` | path | `string` | yes | Drive ID from the workbook item's parentReference.driveId. |
| `driveItemId` | path | `string` | yes | Drive item ID of the Excel workbook file. |
| `persistChanges` | body | `boolean` | yes | Whether changes made in the workbook session are saved to the source workbook. |
