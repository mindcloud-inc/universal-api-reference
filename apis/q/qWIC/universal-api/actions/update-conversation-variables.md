# QWIC: Update Conversation Variables

Updates variables for a QWIC conversation.

```
PUT https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/update-conversation-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QWIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/update-conversation-variables" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "account_id": "string",
  "conversation_id": "string",
  "variables": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/update-conversation-variables', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "account_id": "string",
    "conversation_id": "string",
    "variables": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `account_id` | string | yes | QWIC account ID. |
| `conversation_id` | string | yes | Conversation ID to update. |
| `variables` | list<object> | yes | Conversation/contact variable updates from the QWIC public API docs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native QWIC API, this operation is `POST /v1/accounts/:account_id/conversations/:conversation_id/variables` (base URL `https://app.qwic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation-variables.md) for the provider-specific parameters and requirements.

