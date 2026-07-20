# Better Stack Telemetry: Export Dashboard

Exports a dashboard from Better Stack Telemetry.

```
GET https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/export-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Telemetry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/export-dashboard?connectionId=$CONNECTION_ID&id=164807" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "164807"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/export-dashboard?${params}`, {
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
| `id` | string | yes | The unique identifier of the dashboard or template to export. Example: `164807`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Telemetry API returns.

## Native endpoint

Through the native Better Stack Telemetry API, this operation is `GET /api/v2/dashboards/:id/export` (base URL `https://telemetry.betterstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-dashboard.md) for the provider-specific parameters and requirements.

