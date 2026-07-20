# Reach360: List Group Users

Retrieves all users in a Reach360 group.

```
GET https://connect.mindcloud.co/v1/universal/reach360/latest/actions/list-group-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reach360 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reach360/latest/actions/list-group-users?connectionId=$CONNECTION_ID&limit=25&offset=0&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reach360/latest/actions/list-group-users?${params}`, {
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
| `groupId` | string | yes | The group ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "articulate360User": true,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastActiveAt": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "role": "string"
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
| `firstName` | string |  |
| `id` | string |  |
| `lastActiveAt` | date |  |
| `lastName` | string |  |
| `role` | string |  |

## Native endpoint

Through the native Reach360 API, this operation is `GET /groups/:groupId/users` (base URL `https://api.reach360.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-group-users.md) for the provider-specific parameters and requirements.

