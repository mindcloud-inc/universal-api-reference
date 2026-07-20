# BKK Futar: Search Alerts

Finds active alerts in BKK Futar by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/search-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BKK Futar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/search-alerts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bKKFutar/latest/actions/search-alerts?${params}`, {
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
| `query` | string | no | Search query matched against alert title, description, or identifier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `start` | number | no | Start of the search interval in epoch seconds. |
| `end` | number | no | End of the search interval in epoch seconds. |
| `min_result` | number | no | Minimum number of elements returned. |
| `include_references` | string | no | Reference data to include in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entry": {
        "alertIds": [
          "string"
        ],
        "query": "string",
        "routeIds": [
          "string"
        ],
        "stopIds": [
          "string"
        ]
      },
      "limitExceeded": true,
      "references": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entry.alertIds` | array<string> | Relevant alert IDs found by the alert search. |
| `entry.query` | string | Search query echoed by the API. |
| `entry.routeIds` | array<string> | Relevant route IDs found by the alert search. |
| `entry.stopIds` | array<string> | Relevant stop IDs found by the alert search. |
| `limitExceeded` | boolean | Whether the response exceeded the defined limit. |
| `references` | object | Included reference details. |

## Native endpoint

Through the native BKK Futar API, this operation is `GET /search.json` (base URL `https://futar.bkk.hu/api/query/v1/ws/otp/api/where`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-alerts.md) for the provider-specific parameters and requirements.

