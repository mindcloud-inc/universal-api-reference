# ChatBot: List Stories

Retrieves chatbot story records from ChatBot API.

```
GET https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/list-stories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/list-stories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatBot/latest/actions/list-stories?${params}`, {
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
      "description": "string",
      "id": "string",
      "metrics": [
        {}
      ],
      "name": "Ava Chen",
      "published": true,
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | string |  |
| `metrics` | array<object> |  |
| `name` | string |  |
| `published` | boolean |  |
| `version` | number |  |

## Native endpoint

Through the native ChatBot API, this operation is `GET /v2/stories` (base URL `https://api.chatbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-stories.md) for the provider-specific parameters and requirements.

