# ChatBot: Train Phrases

Trains existing phrases in the ChatBot model.

```
PUT https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/train-phrases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/train-phrases" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/train-phrases', {
  method: 'PUT',
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
      "status": {},
      "timestamp": "2026-05-07T12:00:00.000Z",
      "unused": [
        "string"
      ],
      "used": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | object |  |
| `timestamp` | date |  |
| `unused` | array<string> |  |
| `used` | array<string> |  |

## Native endpoint

Through the native ChatBot API, this operation is `PUT /training/train` (base URL `https://api.chatbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/train-phrases.md) for the provider-specific parameters and requirements.

