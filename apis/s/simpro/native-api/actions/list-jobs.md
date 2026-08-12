# List Jobs with Simpro

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/jobs/`
- **Base URL:** `{buildUrl}/api/v1.0`
- **Official documentation:** [List Jobs](https://developer.simprogroup.com/apidoc/#api-Jobs-get_api_v1_0_companies__companyID__jobs_)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `number` | yes |
| `pageSize` | query | `number` | no |
| `page` | query | `number` | no |
| `limit` | query | `number` | no |
