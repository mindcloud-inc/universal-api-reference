# Groq: List Models

Retrieves models from Groq.

```
GET https://connect.mindcloud.co/v1/universal/groq/latest/actions/list-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Groq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/groq/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/groq/latest/actions/list-models?${params}`, {
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
      "active": true,
      "contextWindow": 1,
      "created": 1,
      "id": "string",
      "maxCompletionTokens": 1,
      "object": "string",
      "ownedBy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `contextWindow` | number |  |
| `created` | number |  |
| `id` | string |  |
| `maxCompletionTokens` | number |  |
| `object` | string |  |
| `ownedBy` | string |  |

## Native endpoint

Through the native Groq API, this operation is `GET /openai/v1/models` (base URL `https://api.groq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-models.md) for the provider-specific parameters and requirements.

