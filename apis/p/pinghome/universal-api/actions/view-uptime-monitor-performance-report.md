# Pinghome: View Uptime Monitor Performance Report

Retrieves an uptime monitor performance report from Pinghome.

```
GET https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/view-uptime-monitor-performance-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/view-uptime-monitor-performance-report?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/view-uptime-monitor-performance-report?${params}`, {
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
| `id` | string | yes | The unique ID of the resource for which statistics are being retrieved. |
| `startDate` | string | no | Specifies the start date for retrieving statistics if needed. |
| `endDate` | string | no | Specifies the end date for retrieving statistics if needed. |
| `interval` | string | no | The aggregation interval for the report. |
| `limit` | number | no | The maximum number of data points to return. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `GET /statistic-query/v1/resource/:id/statistic` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-uptime-monitor-performance-report.md) for the provider-specific parameters and requirements.

