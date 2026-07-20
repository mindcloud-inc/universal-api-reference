# CallTrackingMetrics: List Tracking Sources

Retrieves tracking sources for an account from CallTrackingMetrics.

```
GET https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/list-tracking-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallTrackingMetrics `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/list-tracking-sources?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/list-tracking-sources?${params}`, {
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
      "nextPage": 1,
      "page": 1,
      "perPage": 1,
      "previousPage": 1,
      "sources": [
        [
          {}
        ]
      ],
      "totalEntries": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPage` | number |  |
| `page` | number |  |
| `perPage` | number |  |
| `previousPage` | number |  |
| `sources[]` | array<object> |  |
| `sources[].accountId` | number |  |
| `sources[].description` | string |  |
| `sources[].filterId` | number |  |
| `sources[].geoMode` | string |  |
| `sources[].id` | string |  |
| `sources[].name` | string |  |
| `sources[].online` | boolean |  |
| `sources[].position` | number |  |
| `sources[].url` | string |  |
| `totalEntries` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native CallTrackingMetrics API, this operation is `GET /accounts/:accountId/sources.json` (base URL `https://api.calltrackingmetrics.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tracking-sources.md) for the provider-specific parameters and requirements.

