# Chargeblast: Fetch Alerts

Retrieves alerts from Chargeblast.

```
GET https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/fetch-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeblast `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/fetch-alerts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/fetch-alerts?${params}`, {
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
      "alerts": [
        {}
      ],
      "page": 1,
      "per": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alerts` | array<object> | The alerts returned for the requested page. |
| `page` | number | The current page index returned by Chargeblast. |
| `per` | number | The number of alerts returned per page. |
| `total` | number | The total number of alerts available for the current filters. |

## Native endpoint

Through the native Chargeblast API, this operation is `GET /api/v2/alerts` (base URL `https://api.chargeblast.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/fetch-alerts.md) for the provider-specific parameters and requirements.

