# Get Site By Path with MS SharePoint

Retrieves a SharePoint site by path.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1.0/sites/{{hostname}}:/{{relativePath}}`
- **Base URL:** `https://graph.microsoft.com`
- **Official documentation:** [Get Site By Path](https://learn.microsoft.com/en-us/graph/api/site-getbypath?view=graph-rest-1.0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hostname` | path | `string` | yes | SharePoint hostname, for example contoso.sharepoint.com. |
| `relativePath` | path | `string` | yes | Site path relative to the hostname, for example sites/project-x. |
