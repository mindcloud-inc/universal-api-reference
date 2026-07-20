# Get Site with Microsoft SharePoint Online

Retrieves a site from Microsoft SharePoint Online.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/sites/{{siteId}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Site](https://learn.microsoft.com/en-us/graph/api/site-get?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Microsoft Graph site ID, for example contoso.sharepoint.com,siteCollectionId,siteId. |
