# Chatforma: Create Bot Variable

Creates a new bot variable in Chatforma.

```
POST https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/create-bot-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatforma `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/create-bot-variable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": 1,
  "type": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatforma/latest/actions/create-bot-variable', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": 1,
    "type": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | number | yes | Bot ID that owns the variable |
| `type` | string | yes | Variable type |
| `name` | string | yes | Variable name |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chatforma API returns.

## Native endpoint

Through the native Chatforma API, this operation is `POST /bots/:botId/variables` (base URL `https://api.pro.chatforma.com/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bot-variable.md) for the provider-specific parameters and requirements.

