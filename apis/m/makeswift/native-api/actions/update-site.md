# Update Site with Makeswift

Updates an existing site in Makeswift.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/sites/:siteId`
- **Base URL:** `https://api.makeswift.com`
- **Official documentation:** [Update Site](https://docs.makeswift.com/developer/reference/api/sites/update-site)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | The site ID to update. |
| `name` | body | `string` | no | Updated name for the site. |
