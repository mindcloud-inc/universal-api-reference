# QWIC: Reassign Conversation To Team

Reassigns a QWIC conversation to a team.

```
PUT https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/reassign-conversation-to-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QWIC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/reassign-conversation-to-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversation_id": "string",
  "team.by": "string",
  "team.to": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qWIC/latest/actions/reassign-conversation-to-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversation_id": "string",
    "team.by": "string",
    "team.to": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversation_id` | string | yes | The QWIC conversation identifier. |
| `team.by` | string | yes | The current team identifier. |
| `team.to` | string | yes | The target team identifier. |

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

Through the native QWIC API, this operation is `POST /api/v1/conversation/:conversation_id/events` (base URL `https://app.qwic.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reassign-conversation-to-team.md) for the provider-specific parameters and requirements.

