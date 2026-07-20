# SeaX: Update Conversation

Updates a conversation in the current SeaX workspace.

```
PUT https://connect.mindcloud.co/v1/universal/seaX/latest/actions/update-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/update-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaX/latest/actions/update-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | Conversation identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {},
      "contact_id": "string",
      "contact_labels": [
        {}
      ],
      "created_time": "string",
      "id": "string",
      "is_unread": true,
      "labels": [
        {}
      ],
      "phone": {},
      "phone_id": "string",
      "status": {},
      "updated_time": "string",
      "workspace_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | object |  |
| `contact_id` | string |  |
| `contact_labels` | array<object> |  |
| `created_time` | string |  |
| `id` | string |  |
| `is_unread` | boolean |  |
| `labels` | array<object> |  |
| `phone` | object |  |
| `phone_id` | string |  |
| `status` | object |  |
| `updated_time` | string |  |
| `workspace_id` | string |  |

## Native endpoint

Through the native SeaX API, this operation is `PATCH /conversations/{conversation_id}` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation.md) for the provider-specific parameters and requirements.

