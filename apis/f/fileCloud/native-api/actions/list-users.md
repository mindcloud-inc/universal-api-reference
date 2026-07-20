# List Users with FileCloud

Retrieves users from FileCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/scim/Users`
- **Base URL:** `https://mindcloud.filecloudtrial.com/api/v1`
- **Official documentation:** [List Users](https://fcapi-v1.filecloud.com/#/scim/listScimUsers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | SCIM filter expression. |
| `sortBy` | query | `string` | no | Provider-specific sort field token. Verified values include username and emailid. |
| `sortOrder` | query | `string` | no | Sort direction. Verified values include ascending and descending. |
| `startIndex` | query | `number` | no | 1-based start index. |
| `count` | query | `number` | no | Maximum number of results to return. |
