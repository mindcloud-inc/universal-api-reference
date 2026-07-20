# Create Page with Makeswift

Creates a new page for a site in Makeswift.

## Endpoint

- **Method:** `POST`
- **Path:** `/v6/pages`
- **Base URL:** `https://api.makeswift.com`
- **Official documentation:** [Create Page](https://docs.makeswift.com/developer/reference/api/pages/create-page)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | body | `string` | yes | Site ID where the page will be created. |
| `pathname` | body | `string` | yes | Page pathname (for example /new-page). |
| `name` | body | `string` | yes | Display name for the page. |
