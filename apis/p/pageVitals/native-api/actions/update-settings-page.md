# Update Settings Page with PageVitals

## Endpoint

- **Method:** `PUT`
- **Path:** `/:websiteId/settings/pages/:pageId`
- **Base URL:** `https://api.pagevitals.com`
- **Official documentation:** [Update Settings Page](https://pagevitals.com/docs/rest-api/reference/settings/pages/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `websiteId` | path | `string` | yes |
| `pageId` | path | `string` | yes |
| `url` | body | `string` | no |
| `alias` | body | `string` | no |
