# Testlify: List Workspace Users

Retrieves workspace users from Testlify with optional filters and pagination.

```
GET https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-workspace-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testlify `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-workspace-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testlify/latest/actions/list-workspace-users?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | no | Search query string. |
| `userStatus` | string | no | Filter by workspace user status. |
| `userRole` | string | no | Filter by workspace user role. |
| `userRoleId` | string | no | Filter by user role identifier. |
| `sortBy` | string | no | Column name to sort by. |
| `sortOrder` | string | no | Sort order. |
| `limit` | number | no | Number of items to return. |
| `skip` | number | no | Number of items to skip. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "inviteLink": "https://example.com",
      "isSuperAdmin": true,
      "lastName": "Chen",
      "lastSeenAt": "string",
      "otherJobRole": "string",
      "phoneExt": 1,
      "role": "string",
      "userId": "string",
      "userRoleId": "string",
      "userStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `inviteLink` | string |  |
| `isSuperAdmin` | boolean |  |
| `lastName` | string |  |
| `lastSeenAt` | string |  |
| `otherJobRole` | string |  |
| `phoneExt` | number |  |
| `role` | string |  |
| `userId` | string |  |
| `userRoleId` | string |  |
| `userStatus` | string |  |

## Native endpoint

Through the native Testlify API, this operation is `GET /v1/workspace/team` (base URL `https://api.testlify.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workspace-users.md) for the provider-specific parameters and requirements.

