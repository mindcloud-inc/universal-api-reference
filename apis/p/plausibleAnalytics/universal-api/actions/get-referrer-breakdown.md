# Plausible Analytics: Get Referrer Breakdown

Retrieves referrer breakdown metrics from Plausible Analytics.

```
GET https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/get-referrer-breakdown
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plausible Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/get-referrer-breakdown?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plausibleAnalytics/latest/actions/get-referrer-breakdown?${params}`, {
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
      "dimensions": [
        "string"
      ],
      "metrics": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dimensions` | array<string> |  |
| `metrics` | array<number> |  |

## Native endpoint

Through the native Plausible Analytics API, this operation is `POST /api/v2/query` (base URL `https://plausible.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-referrer-breakdown.md) for the provider-specific parameters and requirements.

