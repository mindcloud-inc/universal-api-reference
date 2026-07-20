# List role privileges with Starburst Galaxy

## Endpoint

- **Method:** `GET`
- **Path:** `/public/api/v1/role/{roleId}/privilege`
- **Base URL:** `https://mindcloud.galaxy.starburst.io`
- **Official documentation:** [List role privileges](https://galaxy.starburst.io/public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `roleId` | path | `string` | yes | Starburst Galaxy role ID. |
| `pageSize` | query | `number` | no | Page size, or 0 for the Starburst Galaxy API default. Current maximum is 100. |
| `pageToken` | query | `string` | no | Pagination token returned by a previous Starburst Galaxy API response. |
| `listAllPrivileges` | query | `boolean` | no | Whether to list all privileges when supported by the Starburst Galaxy API. |
