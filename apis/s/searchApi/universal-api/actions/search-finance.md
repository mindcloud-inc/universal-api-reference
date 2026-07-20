# SearchApi: Search Finance



```
GET https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-finance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SearchApi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-finance?connectionId=$CONNECTION_ID&q=TSLA%3ANASDAQ" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "TSLA:NASDAQ"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-finance?${params}`, {
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
| `q` | string | yes | Example: `TSLA:NASDAQ`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "compareTo": [
        {}
      ],
      "discoverMore": [
        {}
      ],
      "graph": [
        {}
      ],
      "markets": {},
      "searchMetadata": {},
      "searchParameters": {},
      "summary": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `compareTo` | array<object> |  |
| `discoverMore` | array<object> |  |
| `graph` | array<object> |  |
| `markets` | object |  |
| `searchMetadata` | object |  |
| `searchParameters` | object |  |
| `summary` | object |  |

## Native endpoint

Through the native SearchApi API, this operation is `GET /search` (base URL `https://www.searchapi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-finance.md) for the provider-specific parameters and requirements.

