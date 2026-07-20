# Chatvolt AI: Send Location

Sends a location message through Chatvolt AI.

```
POST https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/whatsapp-send-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/whatsapp-send-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "conversationId": "string",
  "latitude": "string",
  "longitude": "string",
  "name": "Ava Chen",
  "address": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/whatsapp-send-location', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "conversationId": "string",
    "latitude": "string",
    "longitude": "string",
    "name": "Ava Chen",
    "address": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | The ID of the agent. |
| `conversationId` | string | yes | The ID of the conversation. |
| `latitude` | string | yes | Latitude of the location. |
| `longitude` | string | yes | Longitude of the location. |
| `name` | string | yes | Name of the place. |
| `address` | string | yes | Address of the place. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Chatvolt AI API returns.

## Native endpoint

Through the native Chatvolt AI API, this operation is `POST /messages/interactive/send-location` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/whatsapp-send-location.md) for the provider-specific parameters and requirements.

