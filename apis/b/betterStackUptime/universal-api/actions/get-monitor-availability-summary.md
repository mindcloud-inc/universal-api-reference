# Better Stack Uptime: Get Monitor Availability Summary

Retrieves an availability summary for a monitor in Better Stack Uptime.

```
GET https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/get-monitor-availability-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Uptime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/get-monitor-availability-summary?connectionId=$CONNECTION_ID&monitorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "monitorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/get-monitor-availability-summary?${params}`, {
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
| `monitorId` | string | yes | The ID of the monitor you want to get availability for |
| `from` | string | no | Start date in YYYY-MM-DD format |
| `to` | string | no | End date in YYYY-MM-DD format |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Uptime API returns.

## Native endpoint

Through the native Better Stack Uptime API, this operation is `GET /v2/monitors/:monitor_id/sla` (base URL `https://uptime.betterstack.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-monitor-availability-summary.md) for the provider-specific parameters and requirements.

