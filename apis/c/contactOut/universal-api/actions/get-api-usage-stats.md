# ContactOut: Get API Usage Stats

Retrieves API usage stats for a month in ContactOut.

```
GET https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-api-usage-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContactOut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-api-usage-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contactOut/latest/actions/get-api-usage-stats?${params}`, {
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
| `period` | string | no | Month to inspect in YYYY-MM format. If omitted, ContactOut uses the current month. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "period": {
        "end": "string",
        "start": "string"
      },
      "status_code": 1,
      "usage": {
        "count": 1,
        "over_quota": 1,
        "phone_count": 1,
        "phone_over_quota": 1,
        "phone_quota": 1,
        "phone_remaining": 1,
        "quota": 1,
        "remaining": 1,
        "search_count": 1,
        "search_over_quota": 1,
        "search_quota": 1,
        "search_remaining": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `period.end` | string |  |
| `period.start` | string |  |
| `status_code` | number |  |
| `usage.count` | number |  |
| `usage.over_quota` | number |  |
| `usage.phone_count` | number |  |
| `usage.phone_over_quota` | number |  |
| `usage.phone_quota` | number |  |
| `usage.phone_remaining` | number |  |
| `usage.quota` | number |  |
| `usage.remaining` | number |  |
| `usage.search_count` | number |  |
| `usage.search_over_quota` | number |  |
| `usage.search_quota` | number |  |
| `usage.search_remaining` | number |  |

## Native endpoint

Through the native ContactOut API, this operation is `GET /v1/stats` (base URL `https://api.contactout.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-api-usage-stats.md) for the provider-specific parameters and requirements.

