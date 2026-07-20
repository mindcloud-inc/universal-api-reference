# Engage: List Users

Retrieves users from Engage with optional email filtering.

```
GET https://connect.mindcloud.co/v1/universal/engage/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Engage `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/engage/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/engage/latest/actions/list-users?${params}`, {
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
| `email` | string | no | Filter the results to users with this email address. Example: `person@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "devices": [
        {}
      ],
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "isAccount": true,
      "lastName": "Chen",
      "lists": [
        {}
      ],
      "memberCount": 1,
      "meta": {},
      "number": "string",
      "segments": [
        {}
      ],
      "stats": {},
      "uid": "string",
      "uidUpdateable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts` | array<object> |  |
| `createdAt` | date |  |
| `devices` | array<object> |  |
| `email` | string |  |
| `firstName` | string |  |
| `id` | string | Engage internal identifier. |
| `isAccount` | boolean |  |
| `lastName` | string |  |
| `lists` | array<object> |  |
| `memberCount` | number |  |
| `meta` | object |  |
| `number` | string | Phone number in international format. |
| `segments` | array<object> |  |
| `stats` | object |  |
| `uid` | string | The user ID supplied by the client application. |
| `uidUpdateable` | boolean | Whether the user ID can still be updated. |

## Native endpoint

Through the native Engage API, this operation is `GET /users` (base URL `https://api.engage.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

