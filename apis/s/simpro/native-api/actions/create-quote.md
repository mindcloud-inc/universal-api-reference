# Create Quote with Simpro

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/:companyId/quotes/`
- **Base URL:** `https://mindcloud.simprosuite.com/api/v1.0`
- **Official documentation:** [Create Quote](https://developer.simprogroup.com/apidoc/#api-Quotes-post_api_v1_0_companies__companyID__quotes_)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `number` | yes |
| `Type` | body | `string` | yes |
| `Site` | body | `number` | yes |
| `Customer` | body | `number` | yes |
| `Description` | body | `string` | no |
