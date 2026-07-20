# Front: Update Conversation

Updates an existing conversation in Front.

```
PUT https://connect.mindcloud.co/v1/universal/front/latest/actions/update-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Front `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/front/latest/actions/update-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "cnv_123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/front/latest/actions/update-conversation', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "cnv_123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | Example: `cnv_123`. |
| `assigneeId` | string | no | ID of the teammate to assign the conversation to. |
| `inboxId` | string | no | ID of the inbox to move the conversation to. |
| `status` | list | no | New status of the conversation. One of: `archived`, `deleted`, `open`, `spam`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `statusId` | string | no | Unique identifier of the status to set. |
| `tagIds[]` | array<string> | no | List of tag IDs replacing the conversation tags. |
| `customFields` | object | no | Conversation custom fields object. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | The raw response body. The saved successful response was an empty string (HTTP 204). |

## Native endpoint

Through the native Front API, this operation is `PATCH /conversations/:conversation_id` (base URL `https://api2.frontapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation.md) for the provider-specific parameters and requirements.

