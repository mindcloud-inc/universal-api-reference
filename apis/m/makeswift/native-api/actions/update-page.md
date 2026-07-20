# Update Page with Makeswift

Updates an existing page in Makeswift.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v6/pages/:pageIdOrPathname`
- **Base URL:** `https://api.makeswift.com`
- **Official documentation:** [Update Page](https://docs.makeswift.com/developer/reference/api/pages/update-page)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageIdOrPathname` | path | `string` | yes | Page ID or pathname to update. |
| `siteId` | query | `string` | yes | The site ID containing the page. |
| `name` | body | `string` | no | Updated page name. |
| `isOnline` | body | `boolean` | no | Whether the page is online. |
