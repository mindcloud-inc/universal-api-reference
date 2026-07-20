# CallTrackingMetrics: List Webhooks

Retrieves webhooks for an account from CallTrackingMetrics.

```
GET https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallTrackingMetrics `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/list-webhooks?${params}`, {
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
      "totalEntries": 1,
      "totalPages": 1,
      "webhooks": [
        [
          {}
        ]
      ]
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
| `totalEntries` | number |  |
| `totalPages` | number |  |
| `webhooks[]` | array<object> |  |
| `webhooks[].accountId` | number |  |
| `webhooks[].clientId` | number |  |
| `webhooks[].clientType` | string |  |
| `webhooks[].id` | number |  |
| `webhooks[].name` | string |  |
| `webhooks[].position` | string |  |
| `webhooks[].weburl` | string |  |
| `webhooks[].withResourceUrl` | boolean |  |

## Native endpoint

Through the native CallTrackingMetrics API, this operation is `GET /accounts/:accountId/webhooks` (base URL `https://api.calltrackingmetrics.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

