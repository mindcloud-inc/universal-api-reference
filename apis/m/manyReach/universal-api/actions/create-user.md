# ManyReach: Create User

Creates a new user in ManyReach.

```
POST https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ManyReach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountType": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/manyReach/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountType": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountType` | string | yes | User permission level. |
| `email` | string | yes | User email address. |
| `firstName` | string | no | User first name. |
| `lastName` | string | no | User last name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emailConfirmed": true,
      "firstName": "Ava",
      "lastName": "Chen",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountType` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `emailConfirmed` | boolean |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native ManyReach API, this operation is `POST https://api.manyreach.com/api/v2/users` (base URL `https://api.manyreach.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

