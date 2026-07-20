# Pinata: Get Time Interval Gateway Analytics

Retrieves time-interval gateway analytics from Pinata.

```
GET https://connect.mindcloud.co/v1/universal/pinata/latest/actions/get-time-interval-gateway-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinata `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinata/latest/actions/get-time-interval-gateway-analytics?connectionId=$CONNECTION_ID&dateInterval=string&endDate=string&gatewayDomain=string&sortBy=string&startDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateInterval": "string",
  "endDate": "string",
  "gatewayDomain": "string",
  "sortBy": "string",
  "startDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinata/latest/actions/get-time-interval-gateway-analytics?${params}`, {
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
| `dateInterval` | string | yes | Date interval (`day` or `week`). |
| `endDate` | string | yes | End date in YYYY-MM-DD format. |
| `gatewayDomain` | string | yes | Gateway domain to analyze. |
| `sortBy` | string | yes | Metric to sort by (`requests` or `bandwidth`). |
| `startDate` | string | yes | Start date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {
        "code": 1,
        "message": "string",
        "reason": "string",
        "request": "string",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error.code` | number | Provider error code for the saved blocked run. |
| `error.message` | string | Provider error message. |
| `error.reason` | string | Provider error reason, when present. |
| `error.request` | string | Provider request identifier. |
| `error.status` | string | Provider error status. |

## Native endpoint

Through the native Pinata API, this operation is `GET /v3/analytics/gateways/time_series` (base URL `https://api.pinata.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-interval-gateway-analytics.md) for the provider-specific parameters and requirements.

