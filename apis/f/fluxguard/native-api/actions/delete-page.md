# Delete Page with Fluxguard

Deletes a monitored page from Fluxguard.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/site/:siteId/session/:sessionId/page/:pageId`
- **Base URL:** `https://api.fluxguard.com`
- **Official documentation:** [Delete Page](https://fluxguard.com/how-to-guides/use-our-api/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `siteId` | path | `string` | yes |
| `sessionId` | path | `string` | yes |
| `pageId` | path | `string` | yes |
