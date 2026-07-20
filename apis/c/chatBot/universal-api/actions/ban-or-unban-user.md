# ChatBot: Ban or Unban User

Updates the ban status of a ChatBot user.

```
PUT https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/ban-or-unban-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/ban-or-unban-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "69baf2590ee62a000879d09c",
  "banned": "false"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/ban-or-unban-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "69baf2590ee62a000879d09c",
    "banned": "false"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | ChatBot user id. Example: `69baf2590ee62a000879d09c`. |
| `banned` | boolean | yes | Whether the user should be banned. Default: `false`. |

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
| `status` | object |  |
| `timestamp` | date |  |

## Native endpoint

Through the native ChatBot API, this operation is `PUT /users/:id/ban` (base URL `https://api.chatbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ban-or-unban-user.md) for the provider-specific parameters and requirements.

