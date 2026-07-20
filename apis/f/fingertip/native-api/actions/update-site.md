# Update Site with Fingertip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/sites/:siteId`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [Update Site](https://docs.fingertip.com/openapi-specs/update-site)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessType` | body | `string` | no | Type of business the site represents, can be null |
| `description` | body | `string` | no | Description of the site, can be null |
| `homePageId` | body | `string` | no | ID of the site's home page, can be null |
| `locationId` | body | `string` | no | ID of the associated location, can be null |
| `name` | body | `string` | no | Name of the site |
| `siteId` | path | `string` | yes | ID of the site to update |
| `slug` | body | `string` | no | URL-friendly identifier for the site |
| `status` | body | `string` | no | Current status of the site |
| `timeZone` | body | `string` | no | Time zone for the site, can be null |
| `workspaceId` | body | `string` | no | ID of the workspace this site belongs to, can be null |
