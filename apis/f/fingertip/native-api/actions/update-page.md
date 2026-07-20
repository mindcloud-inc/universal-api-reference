# Update Page with Fingertip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/pages/:pageId`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [Update Page](https://docs.fingertip.com/openapi-specs/update-page)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Description of the page content, can be null |
| `name` | body | `string` | no | Name of the page, can be null |
| `pageId` | path | `string` | yes | ID of the page to update |
| `position` | body | `number` | no | Display position of the page within the site |
| `siteId` | body | `string` | no | ID of the site this page belongs to |
| `slug` | body | `string` | no | URL-friendly path segment for the page |
