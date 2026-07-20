# Delete Page with Makeswift

Deletes an existing page from Makeswift.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v6/pages/:pageIdOrPathname`
- **Base URL:** `https://api.makeswift.com`
- **Official documentation:** [Delete Page](https://docs.makeswift.com/developer/reference/api/pages/delete-page)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageIdOrPathname` | path | `string` | yes | Page ID or pathname to delete. |
| `siteId` | query | `string` | yes | The site ID containing the page. |
