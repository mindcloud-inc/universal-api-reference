# Engage: Retrieve User

Retrieves a user from Engage by user ID.

```
GET https://connect.mindcloud.co/v1/universal/engage/latest/actions/retrieve-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Engage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/engage/latest/actions/retrieve-user?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/engage/latest/actions/retrieve-user?${params}`, {
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
| `uid` | string | yes | The user ID from your application. |

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

Through the native Engage API, this operation is `GET /users/:uid` (base URL `https://api.engage.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-user.md) for the provider-specific parameters and requirements.

