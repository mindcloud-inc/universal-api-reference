# WotNot: Send API Visitor Slider Response

Creates an API visitor slider response in WotNot.

```
POST https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/send-api-visitor-slider-response
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WotNot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/send-api-visitor-slider-response" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string",
  "message.data.body": "string",
  "message.data.value": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/send-api-visitor-slider-response', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string",
    "message.data.body": "string",
    "message.data.value": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes | API-channel conversation ID |
| `message.data.body` | string | yes | Slider label body |
| `message.data.value` | number | yes | Numeric slider value |
| `message.data.callback` | string | no | Optional callback value |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native WotNot API returns.

## Native endpoint

Through the native WotNot API, this operation is `POST /api/v1/conversation/:conversation_id/messages` (base URL `https://api.wotnot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-api-visitor-slider-response.md) for the provider-specific parameters and requirements.

