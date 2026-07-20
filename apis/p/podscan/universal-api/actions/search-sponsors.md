# Podscan: Search Sponsors

Finds sponsors in Podscan by search text.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/search-sponsors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/search-sponsors?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/search-sponsors?${params}`, {
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
| `query` | string | yes | The sponsor search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {},
      "query": "string",
      "sponsors": [
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
| `pagination` | object |  |
| `query` | string |  |
| `sponsors` | array<object> |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /sponsors/search` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-sponsors.md) for the provider-specific parameters and requirements.

