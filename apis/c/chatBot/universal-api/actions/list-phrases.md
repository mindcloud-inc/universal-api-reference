# ChatBot: List Phrases

Retrieves training phrase records from ChatBot API.

```
GET https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/list-phrases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/list-phrases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/list-phrases?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "items": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Total number of phrases included in the response envelope. |
| `items` | array<object> | Training phrases returned by the ChatBot training endpoint. |

## Native endpoint

Through the native ChatBot API, this operation is `GET /training` (base URL `https://api.chatbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-phrases.md) for the provider-specific parameters and requirements.

