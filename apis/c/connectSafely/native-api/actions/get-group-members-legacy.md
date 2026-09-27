# Get group members (legacy endpoint) with ConnectSafely

Legacy endpoint to retrieve members of a LinkedIn group. Supports multiple input formats: group URL, group URN, or group ID. Returns member profiles with filtering options for membership status and search. Consider using /groups/members or /groups/members-by-url for newer implementations.

## Endpoint

- **Method:** `POST`
- **Path:** `/group-members`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get group members (legacy endpoint)](https://connectsafely.ai/docs/api/linkedin-groups/post-group-members-get-group-members-legacy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `groupUrl` | body | `string` | no | Full LinkedIn group URL (e.g., "https://www.linkedin.com/groups/12345") |
| `groupUrn` | body | `string` | no | LinkedIn group URN (e.g., "urn:li:fsd_group:12345") |
| `groupId` | body | `string` | no | LinkedIn group ID (numeric ID from group URL) |
| `count` | body | `number` | no | Number of members to return per page Default: `10`. |
| `start` | body | `number` | no | Pagination offset (0-indexed) Default: `0`. |
| `membershipStatuses` | body | `array` | no | Filter by membership status: OWNER (group owners), MANAGER (group admins), MEMBER (regular members) Default: `["OWNER", "MANAGER", "MEMBER"]`. |
| `typeaheadQuery` | body | `string` | no | Search query to filter members by name Default: ``. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `groupId` | `string` | The group ID that was queried |
| `accountId` | `string` | LinkedIn account ID used for the request |
| `members` | `array` |  |
| `members[].profileId` | `string` |  |
| `members[].name` | `string` |  |
| `members[].headline` | `string` |  |
| `members[].profileUrl` | `string` |  |
| `members[].profilePicture` | `string` |  |
| `members[].membershipStatus` | `string` |  |
| `pagination` | `object` |  |
| `pagination.start` | `number` |  |
| `pagination.count` | `number` |  |
| `pagination.returned` | `number` |  |
| `filters` | `object` |  |
| `filters.membershipStatuses` | `array` |  |
| `filters.typeaheadQuery` | `string` |  |
| `message` | `string` |  |

## Error status codes

`400`, `403`, `404`. Bodies follow the shared `{ success, code, message }` error shape.
