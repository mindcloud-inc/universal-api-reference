# BodyGraph: Search Locations

Finds locations in BodyGraph by search term.

```
GET https://connect.mindcloud.co/v1/universal/bodyGraph/latest/actions/search-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BodyGraph `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bodyGraph/latest/actions/search-locations?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bodyGraph/latest/actions/search-locations?${params}`, {
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
| `query` | string | yes | A search word to find locations. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admin1": "string",
      "asciiname": "Ava Chen",
      "country": "string",
      "geo": "string",
      "timezone": "string",
      "tokens": [
        "string"
      ],
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin1` | string |  |
| `asciiname` | string |  |
| `country` | string |  |
| `geo` | string |  |
| `timezone` | string |  |
| `tokens` | array<string> |  |
| `value` | string |  |

## Native endpoint

Through the native BodyGraph API, this operation is `GET /v210502/locations` (base URL `https://api.bodygraphchart.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-locations.md) for the provider-specific parameters and requirements.

