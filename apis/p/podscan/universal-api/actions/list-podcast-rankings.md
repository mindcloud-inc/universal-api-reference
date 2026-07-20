# Podscan: List Podcast Rankings

Retrieves podcast ranking data from Podscan.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-podcast-rankings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-podcast-rankings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-podcast-rankings?${params}`, {
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
      "count": 1,
      "filters": {},
      "podcasts": [
        {}
      ],
      "statistics": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `filters` | object |  |
| `podcasts` | array<object> |  |
| `statistics` | object |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /podcasts/rankings` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-podcast-rankings.md) for the provider-specific parameters and requirements.

