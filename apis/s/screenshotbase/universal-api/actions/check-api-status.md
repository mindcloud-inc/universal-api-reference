# Screenshotbase: Check API Status

Retrieves current quota status from Screenshotbase.

```
GET https://connect.mindcloud.co/v1/universal/screenshotbase/latest/actions/check-api-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Screenshotbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/screenshotbase/latest/actions/check-api-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/screenshotbase/latest/actions/check-api-status?${params}`, {
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
      "accountId": 1,
      "quotas": {
        "grace": {
          "remaining": 1,
          "total": 1,
          "used": 1
        },
        "month": {
          "remaining": 1,
          "total": 1,
          "used": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number | The account identifier for the authenticated Screenshotbase account. |
| `quotas` | object | Contains information about the available request quotas. |
| `quotas.grace` | object | Grace quota information. |
| `quotas.grace.remaining` | number | The remaining grace quota. |
| `quotas.grace.total` | number | The total grace quota available. |
| `quotas.grace.used` | number | The used grace quota. |
| `quotas.month` | object | Monthly request quota information. |
| `quotas.month.remaining` | number | The number of monthly requests remaining. |
| `quotas.month.total` | number | The total number of monthly requests available. |
| `quotas.month.used` | number | The number of monthly requests already used. |

## Native endpoint

Through the native Screenshotbase API, this operation is `GET /status` (base URL `https://api.screenshotbase.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-api-status.md) for the provider-specific parameters and requirements.

