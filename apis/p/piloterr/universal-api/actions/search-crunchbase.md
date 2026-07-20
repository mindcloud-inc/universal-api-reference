# Piloterr: Search Crunchbase



```
GET https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/search-crunchbase
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Piloterr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/search-crunchbase?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/search-crunchbase?${params}`, {
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
| `query` | string | yes | Crunchbase search keyword. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": {
        "name": "Ava Chen",
        "permalink": "https://example.com",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results.name` | string |  |
| `results.permalink` | string |  |
| `results.type` | string |  |

## Native endpoint

Through the native Piloterr API, this operation is `GET /crunchbase/search` (base URL `https://api.piloterr.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-crunchbase.md) for the provider-specific parameters and requirements.

