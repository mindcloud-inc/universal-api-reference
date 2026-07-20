# List Groups with FileCloud

Retrieves groups from FileCloud.

## Endpoint

- **Method:** `GET`
- **Path:** `/scim/Groups`
- **Base URL:** `https://mindcloud.filecloudtrial.com/api/v1`
- **Official documentation:** [List Groups](https://fcapi-v1.filecloud.com/#/scim/listScimGroups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `string` | no | SCIM filter expression. |
| `sortBy` | query | `string` | no | Provider-specific sort field token. Verified values include groupname and emailid. |
| `sortOrder` | query | `string` | no | Sort direction. Verified values include ascending and descending. |
| `startIndex` | query | `number` | no | 1-based start index. |
| `count` | query | `number` | no | Maximum number of results to return. |
