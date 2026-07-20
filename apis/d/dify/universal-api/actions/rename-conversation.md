# Dify: Rename Conversation

Updates a conversation name in Dify.

```
PUT https://connect.mindcloud.co/v1/universal/dify/latest/actions/rename-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dify/latest/actions/rename-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "user": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dify/latest/actions/rename-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "user": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | Conversation ID to rename. |
| `name` | string | no | New conversation name. |
| `autoGenerate` | boolean | no | Automatically generate the conversation name. |
| `user` | string | yes | User identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": 1,
      "id": "string",
      "inputs": {},
      "introduction": "string",
      "name": "Ava Chen",
      "status": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number |  |
| `id` | string |  |
| `inputs` | object |  |
| `introduction` | string |  |
| `name` | string |  |
| `status` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Dify API, this operation is `POST /conversations/:conversation_id/name` (base URL `https://api.dify.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rename-conversation.md) for the provider-specific parameters and requirements.

