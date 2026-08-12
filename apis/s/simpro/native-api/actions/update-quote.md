# Update Quote with Simpro

## Endpoint

- **Method:** `PATCH`
- **Path:** `/companies/:companyId/quotes/:quoteId`
- **Base URL:** `{buildUrl}/api/v1.0`
- **Official documentation:** [Update Quote](https://developer.simprogroup.com/apidoc/#api-Quotes-patch_api_v1_0_companies__companyID__quotes__quoteID_)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `number` | yes |
| `quoteId` | path | `number` | yes |
| `Description` | body | `string` | no |
| `Notes` | body | `string` | no |
