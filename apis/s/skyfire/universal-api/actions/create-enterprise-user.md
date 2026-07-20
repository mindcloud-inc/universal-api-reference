# Skyfire: Create Enterprise User

Creates a new enterprise user in Skyfire.

```
POST https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/create-enterprise-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/create-enterprise-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "new.user@example.com",
  "role": "MEMBER"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/create-enterprise-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "new.user@example.com",
    "role": "MEMBER"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The email address of the new Enterprise User or Enterprise Admin User. Example: `new.user@example.com`. |
| `role` | string | yes | The role of the new user. MEMBER for Enterprise User and ADMIN for Enterprise Admin User. Example: `MEMBER`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "buyerAgent": {},
      "userApiKey": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `buyerAgent` | object |  |
| `userApiKey` | string |  |
| `userId` | string |  |

## Native endpoint

Through the native Skyfire API, this operation is `POST /organizations/users` (base URL `https://api.skyfire.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-enterprise-user.md) for the provider-specific parameters and requirements.

