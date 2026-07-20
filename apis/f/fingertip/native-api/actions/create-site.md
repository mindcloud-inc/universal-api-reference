# Create Site with Fingertip

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sites`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [Create Site](https://docs.fingertip.com/openapi-specs/create-site)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the site |
| `slug` | body | `string` | yes | URL-friendly identifier for the site |
| `businessType` | body | `string` | yes | Type of business the site represents |
| `description` | body | `string` | no | Description of the site |
| `status` | body | `string` | no | Current status of the site |
| `locationId` | body | `string` | no | ID of the associated location |
| `homePageId` | body | `string` | no | ID of the site's home page |
| `timeZone` | body | `string` | no | Time zone for the site |
| `workspaceId` | body | `string` | no | ID of the workspace this site belongs to |
