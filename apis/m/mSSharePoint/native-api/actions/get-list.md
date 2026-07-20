# Get List with MS SharePoint

Retrieves a SharePoint list.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/sites/{{siteId}}/lists/{{listId}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get List](https://learn.microsoft.com/en-us/graph/api/list-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Microsoft Graph SharePoint site ID. |
| `listId` | path | `string` | yes | SharePoint list ID. |
