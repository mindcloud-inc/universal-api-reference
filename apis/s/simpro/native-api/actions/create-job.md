# Create Job with Simpro

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/:companyId/jobs/`
- **Base URL:** `https://mindcloud.simprosuite.com/api/v1.0`
- **Official documentation:** [Create Job](https://developer.simprogroup.com/apidoc/#api-Jobs-post_api_v1_0_companies__companyID__jobs_)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `number` | yes |
| `Type` | body | `string` | yes |
| `Site` | body | `number` | yes |
| `Customer` | body | `number` | no |
| `Description` | body | `string` | no |
