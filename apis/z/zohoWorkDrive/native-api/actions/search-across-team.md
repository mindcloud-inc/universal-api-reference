# Search across Team with Zoho WorkDrive

Finds files and folders in Zoho WorkDrive across a team.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/teams/:teamId/records`
- **Base URL:** `{api_domain}/workdrive`
- **Official documentation:** [Search across Team](https://workdrive.zoho.com/apidocs/v1/search/searchacrossteam)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | The WorkDrive team ID. |
| `search[all]` | query | `string` | no | Search text to match across names or content. |
| `filter[parentId]` | query | `string` | no | Restrict the search to a specific parent folder. |
| `filter[type]` | query | `string` | no | Filter the results by resource type. |
| `filter[date]` | query | `string` | no | Use a predefined date filter range. |
| `filter[fromDate]` | query | `string` | no | Start date for the filter range. |
| `filter[toDate]` | query | `string` | no | End date for the filter range. |
| `filter[status]` | query | `string` | no | Filter by the WorkDrive file status. |
| `filter[creator]` | query | `string` | no | Filter by the creator of the resource. |
| `page[limit]` | query | `string` | no | Maximum number of records to return. |
| `page[offset]` | query | `string` | no | Number of records to skip before returning results. |
| `sort` | query | `string` | no | Sort expression for the returned resources. |
