# ChatBot: Create Story

Creates a new story in ChatBot API.

```
POST https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/create-story
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/create-story" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/create-story', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": {},
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `status` | object |  |
| `timestamp` | date |  |

## Native endpoint

Through the native ChatBot API, this operation is `POST /v2/stories` (base URL `https://api.chatbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-story.md) for the provider-specific parameters and requirements.

