# Pinghome: View Uptime Monitor State Change History

Retrieves uptime monitor state change history from Pinghome.

```
GET https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/view-uptime-monitor-state-change-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/view-uptime-monitor-state-change-history?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/view-uptime-monitor-state-change-history?${params}`, {
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
| `id` | string | yes | The unique ID of the uptime monitor. |
| `startDate` | string | no | Start date to retrieve logs from. |
| `endDate` | string | no | End date to retrieve logs until. |
| `limit` | number | no | The maximum number of log entries to return. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `GET /statistic-query/v1/resource/:id/state-changed-logs` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-uptime-monitor-state-change-history.md) for the provider-specific parameters and requirements.

