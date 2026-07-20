# Add Page with Fluxguard

Adds a new page for monitoring in Fluxguard.

## Endpoint

- **Method:** `POST`
- **Path:** `/add-page`
- **Base URL:** `https://api.fluxguard.com`
- **Official documentation:** [Add Page](https://fluxguard.com/how-to-guides/use-our-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The URL to monitor. |
| `siteId` | body | `string` | no | Existing site identifier to attach the page to. |
| `sessionId` | body | `string` | no | Existing session identifier to attach the page to. |
| `categoryId` | body | `string` | no | Category ID for the new site when creating one. |
| `categoryName` | body | `string` | no | Category name for the new site when creating one. |
| `siteNickname` | body | `string` | no | Nickname for the new site. |
