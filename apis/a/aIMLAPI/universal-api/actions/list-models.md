# AI/ML API: List Models

Retrieves available model IDs from AI/ML API.

```
GET https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/list-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AI/ML API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aIMLAPI/latest/actions/list-models?${params}`, {
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
      "endpoints": [
        "string"
      ],
      "features": [
        "string"
      ],
      "id": "string",
      "info": {
        "contextLength": 1,
        "description": "string",
        "developer": "string",
        "docsUrl": "https://example.com",
        "maxTokens": 1,
        "name": "Ava Chen",
        "url": "https://example.com"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endpoints[]` | string |  |
| `features[]` | string |  |
| `id` | string |  |
| `info.contextLength` | number |  |
| `info.description` | string |  |
| `info.developer` | string |  |
| `info.docsUrl` | string |  |
| `info.maxTokens` | number |  |
| `info.name` | string |  |
| `info.url` | string |  |
| `type` | string |  |

## Native endpoint

Through the native AI/ML API API, this operation is `GET /models` (base URL `https://api.aimlapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-models.md) for the provider-specific parameters and requirements.

