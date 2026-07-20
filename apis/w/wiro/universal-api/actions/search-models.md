# Wiro: Search Models

Finds AI models in Wiro by keyword or category.

```
GET https://connect.mindcloud.co/v1/universal/wiro/latest/actions/search-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wiro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiro/latest/actions/search-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wiro/latest/actions/search-models?${params}`, {
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
      "errors": [
        "string"
      ],
      "result": true,
      "tool": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `result` | boolean |  |
| `tool` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native Wiro API, this operation is `POST /Tool/List` (base URL `https://api.wiro.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-models.md) for the provider-specific parameters and requirements.

