# Reach360: List Users

Retrieves all users from Reach360.

```
GET https://connect.mindcloud.co/v1/universal/reach360/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reach360 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reach360/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reach360/latest/actions/list-users?${params}`, {
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
| `email` | string | no | Only return users with this email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "articulate360User": true,
      "email": "ava@example.com",
      "favoritesUrl": "https://example.com",
      "firstName": "Ava",
      "groupsUrl": "https://example.com",
      "id": "string",
      "lastActiveAt": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "learnerReportUrl": "https://example.com",
      "managingGroupsUrl": "https://example.com",
      "reportingGroupsUrl": "https://example.com",
      "role": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `articulate360User` | boolean |  |
| `email` | string |  |
| `favoritesUrl` | string |  |
| `firstName` | string |  |
| `groupsUrl` | string |  |
| `id` | string |  |
| `lastActiveAt` | date |  |
| `lastName` | string |  |
| `learnerReportUrl` | string |  |
| `managingGroupsUrl` | string |  |
| `reportingGroupsUrl` | string |  |
| `role` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Reach360 API, this operation is `GET /users` (base URL `https://api.reach360.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

