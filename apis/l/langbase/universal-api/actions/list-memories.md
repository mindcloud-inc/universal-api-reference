# Langbase: List Memories



```
GET https://connect.mindcloud.co/v1/universal/langbase/latest/actions/list-memories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langbase/latest/actions/list-memories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langbase/latest/actions/list-memories?${params}`, {
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
      "embeddingModel": "string",
      "name": "Ava Chen",
      "ownerLogin": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `embeddingModel` | string |  |
| `name` | string |  |
| `ownerLogin` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Langbase API, this operation is `GET v1/memory` (base URL `https://api.langbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-memories.md) for the provider-specific parameters and requirements.

