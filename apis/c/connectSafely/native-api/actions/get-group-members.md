# Get group members by group ID with ConnectSafely

Retrieve members of a LinkedIn group by its ID. Returns profile information for group members including name, headline, profile picture, and membership status. Useful for lead generation, networking, and community analysis. Requires membership in the group to access member list. **Rate limit: 1000 members per day per LinkedIn account.**

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/members`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get group members by group ID](https://connectsafely.ai/docs/api/linkedin-groups/post-groups-members-get-group-members)

## Quota

1000 group members per day per LinkedIn account. The count is based on total members fetched across all requests.

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | body | `string` | no | LinkedIn account ID to use. If not provided, uses the default account. |
| `groupId` | body | `string` | yes | LinkedIn group ID (numeric ID from group URL) |
| `count` | body | `number` | no | Number of members to return per page (max 100) Default: `50`. |
| `start` | body | `number` | no | Pagination offset (0-indexed) Default: `0`. |
| `membershipStatuses` | body | `array` | no | Filter by membership status: OWNER (group owners), MANAGER (group admins), MEMBER (regular members) Default: `["OWNER", "MANAGER", "MEMBER"]`. |
| `typeaheadQuery` | body | `string` | no | Search query to filter members by name Default: ``. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `accountId` | `string` | LinkedIn account ID used for the request |
| `groupId` | `string` | The group ID that was queried |
| `members` | `array` |  |
| `members[].entityUrn` | `string` | LinkedIn entity URN for the member |
| `members[].publicIdentifier` | `string` | LinkedIn public identifier (vanity name) |
| `members[].firstName` | `string` |  |
| `members[].lastName` | `string` |  |
| `members[].headline` | `string` |  |
| `members[].profilePicture` | `string` | URL to profile picture |
| `members[].membershipStatus` | `list` | Role in the group |
| `pagination` | `object` |  |
| `pagination.start` | `number` |  |
| `pagination.count` | `number` |  |
| `pagination.total` | `number` |  |
| `hasMore` | `boolean` | Whether more members are available |
| `count` | `number` | Number of members returned in this response |

## Error status codes

`400`, `429`. Bodies follow the shared `{ success, code, message }` error shape.
