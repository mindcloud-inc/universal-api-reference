# Get Page with Makeswift

Retrieves a page from Makeswift.

## Endpoint

- **Method:** `GET`
- **Path:** `/v6/pages/:pageIdOrPathname`
- **Base URL:** `https://api.makeswift.com`
- **Official documentation:** [Get Page](https://docs.makeswift.com/developer/reference/api/pages/get-page)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageIdOrPathname` | path | `string` | yes | Page ID or pathname. |
| `siteId` | query | `string` | yes | The site ID containing the page. |
| `locale` | query | `string` | no | Read page data for a specific locale. |
| `versionRef` | query | `string` | no | Version reference for preview/published content. |
