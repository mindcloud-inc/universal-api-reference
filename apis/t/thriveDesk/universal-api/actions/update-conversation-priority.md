# ThriveDesk: Update Conversation Priority



```
PUT https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/update-conversation-priority
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThriveDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/update-conversation-priority" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/thriveDesk/latest/actions/update-conversation-priority', {
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
| `conversationId` | string | yes | The conversation ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "id": "string",
      "status": "string",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Raw conversation payload. |
| `id` | string | Conversation identifier. |
| `status` | string | Conversation status when returned. |
| `subject` | string | Conversation subject when returned. |

## Native endpoint

Through the native ThriveDesk API, this operation is `PUT /v1/conversation/{{conversationId}}/update/priority` (base URL `https://api.thrivedesk.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation-priority.md) for the provider-specific parameters and requirements.

