# SEOTakeoff: List Keywords



```
GET https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/list-keywords
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SEOTakeoff `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/list-keywords?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/list-keywords?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "cluster_id": "string",
      "cluster_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "difficulty": 1,
      "id": "string",
      "keyword": "string",
      "volume": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cluster_id` | string |  |
| `cluster_name` | string |  |
| `created_at` | date |  |
| `difficulty` | number |  |
| `id` | string |  |
| `keyword` | string |  |
| `volume` | number |  |

## Native endpoint

Through the native SEOTakeoff API, this operation is `GET /api/zapier/keywords` (base URL `https://api.seotakeoff.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-keywords.md) for the provider-specific parameters and requirements.

