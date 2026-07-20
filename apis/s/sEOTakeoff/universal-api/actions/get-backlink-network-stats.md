# SEOTakeoff: Get Backlink Network Stats



```
GET https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/get-backlink-network-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SEOTakeoff `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/get-backlink-network-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/get-backlink-network-stats?${params}`, {
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
      "accepted_proposals": 1,
      "active_members": 1,
      "implemented_links": 1,
      "total_members": 1,
      "total_proposals": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accepted_proposals` | number |  |
| `active_members` | number |  |
| `implemented_links` | number |  |
| `total_members` | number |  |
| `total_proposals` | number |  |

## Native endpoint

Through the native SEOTakeoff API, this operation is `GET /api/v1/backlink-network/stats` (base URL `https://api.seotakeoff.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-backlink-network-stats.md) for the provider-specific parameters and requirements.

