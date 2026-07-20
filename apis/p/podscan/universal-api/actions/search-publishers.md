# Podscan: Search Publishers

Finds publishers in Podscan by search text.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/search-publishers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/search-publishers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/search-publishers?${params}`, {
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
| `query` | string | no | The publisher search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filters": {},
      "pagination": {},
      "publishers": [
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
| `filters` | object |  |
| `pagination` | object |  |
| `publishers` | array<object> |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /publishers/search` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-publishers.md) for the provider-specific parameters and requirements.

