# Chatling: Duplicate Chatbot

Creates a duplicate chatbot in Chatling.

```
POST https://connect.mindcloud.co/v1/universal/chatling/latest/actions/duplicate-chatbot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatling/latest/actions/duplicate-chatbot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chatbotId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatling/latest/actions/duplicate-chatbot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chatbotId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chatbotId` | string | yes | The chatbot ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chatbotId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chatbotId` | string |  |

## Native endpoint

Through the native Chatling API, this operation is `POST /chatbots/:chatbotId/duplicate` (base URL `https://api.chatling.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-chatbot.md) for the provider-specific parameters and requirements.

