# Papyrs: Search Results



```
GET https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/search-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Papyrs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/search-results?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "q": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/papyrs/latest/actions/search-results?${params}`, {
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
| `q` | string | yes | The Papyrs search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "cat": "string",
          "desc": "string",
          "icon": "string",
          "id": "string",
          "lnk": "string",
          "weight": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> | Search results. |
| `results[].cat` | string | Result category. |
| `results[].desc` | string | Search result description. |
| `results[].icon` | string | Papyrs icon class for the result. |
| `results[].id` | string | Papyrs object ID. |
| `results[].lnk` | string | Relative result link. |
| `results[].weight` | number | Search relevance score. |

## Native endpoint

Through the native Papyrs API, this operation is `GET /search/query/` (base URL `https://{{credentials.subdomain}}.papyrs.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-results.md) for the provider-specific parameters and requirements.

