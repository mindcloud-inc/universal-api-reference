# Get Page Data with Fluxguard

Retrieves data for a monitored page from Fluxguard.

## Endpoint

- **Method:** `GET`
- **Path:** `/site/:siteId/session/:sessionId/page/:pageId`
- **Base URL:** `https://api.fluxguard.com`
- **Official documentation:** [Get Page Data](https://fluxguard.com/how-to-guides/use-our-api/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `siteId` | path | `string` | yes |
| `sessionId` | path | `string` | yes |
| `pageId` | path | `string` | yes |
