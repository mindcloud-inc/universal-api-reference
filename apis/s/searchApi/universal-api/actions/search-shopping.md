# SearchApi: Search Shopping



```
GET https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-shopping
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SearchApi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-shopping?connectionId=$CONNECTION_ID&q=PS5" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "PS5"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-shopping?${params}`, {
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
| `q` | string | yes | Shopping search query. Example: `PS5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allFiltersToken": "string",
      "filters": [
        {}
      ],
      "searchInformation": {},
      "searchMetadata": {},
      "searchParameters": {},
      "shoppingResults": [
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
| `allFiltersToken` | string |  |
| `filters` | array<object> |  |
| `searchInformation` | object |  |
| `searchMetadata` | object |  |
| `searchParameters` | object |  |
| `shoppingResults` | array<object> |  |

## Native endpoint

Through the native SearchApi API, this operation is `GET /search` (base URL `https://www.searchapi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-shopping.md) for the provider-specific parameters and requirements.

