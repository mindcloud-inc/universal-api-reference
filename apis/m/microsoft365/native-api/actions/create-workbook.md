# Create Workbook with Microsoft 365

Creates a workbook in Microsoft 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1.0/me/drive/root/children`
- **Base URL:** `https://graph.microsoft.com`
- **API:** REST (skip pagination)
- **Official documentation:** [Create Workbook](https://learn.microsoft.com/en-us/graph/api/driveitem-post-children?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Excel workbook file name including the .xlsx extension. |
