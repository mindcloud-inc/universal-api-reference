# Create Page with Fingertip

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sites/:siteId/pages`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [Create Page](https://docs.fingertip.com/openapi-specs/create-page)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | ID of the site to create a page in |
| `slug` | body | `string` | yes | URL-friendly path segment for the page |
| `name` | body | `string` | yes | Name of the page |
| `siteId` | body | `string` | yes | ID of the site this page belongs to |
| `description` | body | `string` | no | Description of the page content |
| `position` | body | `number` | no | Display position of the page within the site |
