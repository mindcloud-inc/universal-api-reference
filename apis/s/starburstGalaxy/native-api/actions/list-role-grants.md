# List role grants with Starburst Galaxy

## Endpoint

- **Method:** `GET`
- **Path:** `/public/api/v1/role/{roleId}/rolegrant`
- **Base URL:** `https://mindcloud.galaxy.starburst.io`
- **Official documentation:** [List role grants](https://galaxy.starburst.io/public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roleId` | path | `string` | yes | Starburst Galaxy role ID. |
| `pageSize` | query | `number` | no | Page size, or 0 for the Starburst Galaxy API default. Current maximum is 100. |
| `pageToken` | query | `string` | no | Pagination token returned by a previous Starburst Galaxy API response. |
| `type` | query | `string` | no | Optional role grant type filter documented by the Starburst Galaxy API. |
