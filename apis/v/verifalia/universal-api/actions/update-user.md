# Verifalia: Update User

Updates an existing user in Verifalia.

```
PUT https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Verifalia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/verifalia/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | The Verifalia user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authentication": {},
      "authorization": {},
      "defaults": {},
      "displayName": "Ava Chen",
      "isActive": true,
      "preferredContactMethod": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authentication` | object | Authentication settings for the user. |
| `authorization` | object | Authorization settings for the user. |
| `defaults` | object | Default user-level settings such as retention. |
| `displayName` | string | The user's display name. |
| `isActive` | boolean | Whether the user is active. |
| `preferredContactMethod` | string | The preferred contact-method ID when configured. |
| `type` | string | The Verifalia user type. |

## Native endpoint

Through the native Verifalia API, this operation is `PATCH /users/{user-id}` (base URL `https://api-1.verifalia.com/v2.7`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

