# Engage: Update User Attributes

Updates a user in Engage, or creates one if missing.

```
PUT https://connect.mindcloud.co/v1/universal/engage/latest/actions/update-user-attributes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Engage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/engage/latest/actions/update-user-attributes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/engage/latest/actions/update-user-attributes', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `createdAt` | string | no | The signup or creation timestamp for the user. |
| `devicePlatform` | string | no | The device platform, such as android or ios. |
| `deviceToken` | string | no | The user’s device token. |
| `email` | string | no | The user’s email address. |
| `firstName` | string | no | The user’s first name. |
| `isAccount` | boolean | no | Set to true to convert or create the entity as an account. |
| `lastName` | string | no | The user’s last name. |
| `meta` | object | no | Additional user attributes as an object. |
| `number` | string | no | The user’s phone number in international format. |
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

Through the native Engage API, this operation is `PUT /users/:uid` (base URL `https://api.engage.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-attributes.md) for the provider-specific parameters and requirements.

