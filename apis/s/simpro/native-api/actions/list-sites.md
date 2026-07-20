# List Sites with Simpro

## Endpoint

- **Method:** `GET`
- **Path:** `/companies/:companyId/sites/`
- **Base URL:** `https://mindcloud.simprosuite.com/api/v1.0`
- **Official documentation:** [List Sites](https://developer.simprogroup.com/apidoc/?page=3faa64303d5f5bcd043bb88f6768e603)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `number` | yes | Simpro company ID. Single-company builds usually use 0. |
| `pageSize` | query | `number` | no | Maximum sites per page. |
| `page` | query | `number` | no | Page number. |
| `limit` | query | `number` | no | Hard limit for number of results. |
