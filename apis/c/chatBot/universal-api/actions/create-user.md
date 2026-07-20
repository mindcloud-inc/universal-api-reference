# ChatBot: Create User

Creates a new user in ChatBot API.

```
POST https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "codex-user-20260318",
  "attributes.default_name": "Codex Test User"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "codex-user-20260318",
    "attributes.default_name": "Codex Test User"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | External user identifier. Example: `codex-user-20260318`. |
| `attributes.default_name` | string | yes | User display name. Example: `Codex Test User`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": {},
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created user identifier. |
| `status` | object | Mutation status payload returned by ChatBot. |
| `timestamp` | date | Timestamp returned by ChatBot for the mutation. |

## Native endpoint

Through the native ChatBot API, this operation is `POST /users` (base URL `https://api.chatbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

