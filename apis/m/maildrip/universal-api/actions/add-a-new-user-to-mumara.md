# Maildrip: Add a new user to Mumara



```
POST https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/add-a-new-user-to-mumara
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Maildrip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/add-a-new-user-to-mumara" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "email": "ava@example.com",
  "password": "string",
  "packageId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/add-a-new-user-to-mumara', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "email": "ava@example.com",
    "password": "string",
    "packageId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | User's full name |
| `email` | string | yes | User's email address |
| `password` | string | yes | User's password |
| `passwordConfirmation` | string | no | Confirmation of the user's password |
| `packageId` | number | yes | Package/plan ID for the user |
| `timezone` | string | no | User's timezone |
| `loginIps` | string | no | Comma-separated allowed IP addresses |
| `hashed` | boolean | no | Whether password is already hashed |
| `response` | number | no | Response format type |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `success` | boolean |  |

## Native endpoint

Through the native Maildrip API, this operation is `POST /api/v1/mumara/users` (base URL `https://api.maildrip.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-a-new-user-to-mumara.md) for the provider-specific parameters and requirements.

