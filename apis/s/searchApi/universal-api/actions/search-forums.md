# SearchApi: Search Forums



```
GET https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-forums
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SearchApi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-forums?connectionId=$CONNECTION_ID&q=ChatGPT" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "ChatGPT"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/search-forums?${params}`, {
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
| `q` | string | yes | Example: `ChatGPT`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "organicResults": [
        {}
      ],
      "pagination": {},
      "searchInformation": {},
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
| `organicResults` | array<object> |  |
| `pagination` | object |  |
| `searchInformation` | object |  |
| `searchMetadata` | object |  |
| `searchParameters` | object |  |

## Native endpoint

Through the native SearchApi API, this operation is `GET /search` (base URL `https://www.searchapi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-forums.md) for the provider-specific parameters and requirements.

