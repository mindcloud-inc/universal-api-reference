# Better Stack Uptime: Delete Monitor

Deletes an existing monitor from Better Stack Uptime.

```
DELETE https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/delete-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Uptime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/delete-monitor?connectionId=$CONNECTION_ID&monitorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "monitorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/delete-monitor?${params}`, {
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
| `monitorId` | string | yes | The monitor ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Uptime API returns.

## Native endpoint

Through the native Better Stack Uptime API, this operation is `DELETE /v2/monitors/:monitor_id` (base URL `https://uptime.betterstack.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-monitor.md) for the provider-specific parameters and requirements.

