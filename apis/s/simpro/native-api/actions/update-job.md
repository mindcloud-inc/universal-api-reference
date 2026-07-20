# Update Job with Simpro

## Endpoint

- **Method:** `PATCH`
- **Path:** `/companies/:companyId/jobs/:jobId`
- **Base URL:** `https://mindcloud.simprosuite.com/api/v1.0`
- **Official documentation:** [Update Job](https://developer.simprogroup.com/apidoc/#api-Jobs-patch_api_v1_0_companies__companyID__jobs__jobID_)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `companyId` | path | `number` | yes |
| `jobId` | path | `number` | yes |
| `Description` | body | `string` | no |
| `Notes` | body | `string` | no |
