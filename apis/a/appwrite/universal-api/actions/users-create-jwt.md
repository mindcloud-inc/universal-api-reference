# Appwrite: Create user JWT

Creates a new user JWT in your Appwrite project.

```
POST https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-create-jwt
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-create-jwt" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-create-jwt', {
  method: 'POST',
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
| `userId` | string | yes | User ID. |
| `sessionId` | string | no | Session ID. Use the string 'recent' to use the most recent session. Defaults to the most recent session. |
| `duration` | number | no | Time in seconds before JWT expires. Default duration is 900 seconds, and maximum is 3600 seconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jwt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jwt` | string | JWT encoded string. |

## Native endpoint

Through the native Appwrite API, this operation is `POST /users/{userId}/jwts` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/users-create-jwt.md) for the provider-specific parameters and requirements.

