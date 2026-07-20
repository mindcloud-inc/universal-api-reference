# Rossum: Create User

Creates a new user in Rossum.

```
POST https://connect.mindcloud.co/v1/universal/rossum/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rossum `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rossum/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com",
  "username": "Ava Chen",
  "organization": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rossum/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen",
    "email": "ava@example.com",
    "username": "Ava Chen",
    "organization": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | First name of the user. |
| `lastName` | string | yes | Last name of the user. |
| `email` | string | yes | Email address for the new user. |
| `username` | string | yes | Rossum username for the new user, typically the same as the email. |
| `organization` | string | yes | Organization URL that owns the user. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authType": "string",
      "dateJoined": "string",
      "deleted": true,
      "email": "ava@example.com",
      "emailVerified": true,
      "firstName": "Ava",
      "id": 1,
      "isActive": true,
      "lastLogin": {},
      "lastName": "Chen",
      "oidcId": {},
      "organization": "string",
      "phoneNumber": {},
      "uiSettings": {
        "complexLineItems": true
      },
      "url": "https://example.com",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authType` | string |  |
| `dateJoined` | string |  |
| `deleted` | boolean |  |
| `email` | string |  |
| `emailVerified` | boolean |  |
| `firstName` | string |  |
| `id` | number |  |
| `isActive` | boolean |  |
| `lastLogin` | object |  |
| `lastName` | string |  |
| `oidcId` | object |  |
| `organization` | string |  |
| `phoneNumber` | object |  |
| `uiSettings.complexLineItems` | boolean |  |
| `url` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Rossum API, this operation is `POST /users` (base URL `https://mindcloud.rossum.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

