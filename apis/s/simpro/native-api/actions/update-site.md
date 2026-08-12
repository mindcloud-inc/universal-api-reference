# Update Site with Simpro

## Endpoint

- **Method:** `PATCH`
- **Path:** `/companies/:companyId/sites/:siteId`
- **Base URL:** `{buildUrl}/api/v1.0`
- **Official documentation:** [Update Site](https://developer.simprogroup.com/apidoc/#api-Sites-patch_api_v1_0_companies__companyID__sites__siteID_)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `number` | yes |
| `siteId` | path | `number` | yes |
| `Name` | body | `string` | no |
| `PublicNotes` | body | `string` | no |
