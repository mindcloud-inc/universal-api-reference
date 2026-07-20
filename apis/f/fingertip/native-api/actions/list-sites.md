# List Sites with Fingertip

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/sites`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [List Sites](https://docs.fingertip.com/openapi-specs/list-sites)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Pagination cursor |
| `pageSize` | query | `string` | no | Number of items per page (default: 10, max: 25) |
| `search` | query | `string` | no | Search query |
| `sortBy` | query | `string` | no | Field to sort by (default: updatedAt) |
| `sortDirection` | query | `string` | no | Sort direction (default: desc) |
| `statuses` | query | `string` | no | Filter sites by status |
| `workspaceId` | query | `string` | no | Filter sites by workspace ID |
