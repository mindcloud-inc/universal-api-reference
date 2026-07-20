# SearchApi: Get Autocomplete Suggestions



```
GET https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/get-autocomplete-suggestions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SearchApi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/get-autocomplete-suggestions?connectionId=$CONNECTION_ID&q=ama" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "ama"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/get-autocomplete-suggestions?${params}`, {
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
| `q` | string | yes | Example: `ama`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "searchMetadata": {},
      "searchParameters": {},
      "suggestions": [
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
| `searchMetadata` | object |  |
| `searchParameters` | object |  |
| `suggestions` | array<object> |  |

## Native endpoint

Through the native SearchApi API, this operation is `GET /search` (base URL `https://www.searchapi.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-autocomplete-suggestions.md) for the provider-specific parameters and requirements.

