# ChatBot: Update User

Updates an existing user in ChatBot API.

```
PUT https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/update-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/update-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "69bae98566f10f0007c4e5eb",
  "attributes.default_name": "Codex Updated User"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/update-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "69bae98566f10f0007c4e5eb",
    "attributes.default_name": "Codex Updated User"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ChatBot user id. Example: `69bae98566f10f0007c4e5eb`. |
| `attributes.default_name` | string | yes | Updated user display name. Example: `Codex Updated User`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `status` | object | Mutation status payload returned by ChatBot. |
| `timestamp` | date | Timestamp returned by ChatBot for the mutation. |

## Native endpoint

Through the native ChatBot API, this operation is `PUT /users/:id` (base URL `https://api.chatbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user.md) for the provider-specific parameters and requirements.

