# SearchApi: Search Trends



```
GET https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-trends
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SearchApi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-trends?connectionId=$CONNECTION_ID&q=Java%2CPython%2CRuby%2CAssembly%2CJavaScript" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "Java,Python,Ruby,Assembly,JavaScript"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-trends?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `q` | string | yes | Example: `Java,Python,Ruby,Assembly,JavaScript`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "interestOverTime": {},
      "searchMetadata": {},
      "searchParameters": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `interestOverTime` | object |  |
| `searchMetadata` | object |  |
| `searchParameters` | object |  |

## Native endpoint

Through the native SearchApi API, this operation is `GET /search` (base URL `https://www.searchapi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-trends.md) for the provider-specific parameters and requirements.

