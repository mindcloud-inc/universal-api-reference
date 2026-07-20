# WotNot: Update Conversation Variables

Updates conversation variables in WotNot.

```
PUT https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/update-conversation-variables
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WotNot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/update-conversation-variables" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "conversationId": "string",
  "variables[0].name": "Ava Chen",
  "variables[0].type": "string",
  "variables[0].value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/update-conversation-variables', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "conversationId": "string",
    "variables[0].name": "Ava Chen",
    "variables[0].type": "string",
    "variables[0].value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | number | yes | WotNot account ID |
| `conversationId` | string | yes | Conversation ID |
| `variables[0].name` | string | yes | Variable name |
| `variables[0].type` | string | yes | Variable scope type |
| `variables[0].value` | string | yes | Variable value |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WotNot API returns.

## Native endpoint

Through the native WotNot API, this operation is `POST /v1/accounts/:account_id/conversations/:conversation_id/variables` (base URL `https://api.wotnot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation-variables.md) for the provider-specific parameters and requirements.

