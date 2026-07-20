# SparrowDesk: Add Conversation Reply

Creates a conversation reply in SparrowDesk.

```
POST https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/add-conversation-reply
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparrowDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/add-conversation-reply" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "replyText": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/add-conversation-reply', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "replyText": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | SparrowDesk conversation ID. |
| `replyText` | string | yes | Reply or internal note content. |
| `type` | string | yes | REPLY or INTERNAL_NOTE. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the reply was created successfully. |

## Native endpoint

Through the native SparrowDesk API, this operation is `POST /conversations/{{id}}/reply` (base URL `https://api.sparrowdesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-conversation-reply.md) for the provider-specific parameters and requirements.

