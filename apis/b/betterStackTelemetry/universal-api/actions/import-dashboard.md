# Better Stack Telemetry: Import Dashboard

Imports a dashboard into Better Stack Telemetry.

```
POST https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/import-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Telemetry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/import-dashboard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "mc-stage3-dashboard-roundtrip",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/import-dashboard', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "mc-stage3-dashboard-roundtrip",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | A name for the new dashboard. Example: `mc-stage3-dashboard-roundtrip`. |
| `data` | object | yes | The dashboard configuration data in JSON format, typically obtained from the Export Dashboard endpoint. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamName` | string | no | Required if using a global API token to specify the team which should own the resource. Example: `example-team`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Telemetry API returns.

## Native endpoint

Through the native Better Stack Telemetry API, this operation is `POST /api/v2/dashboards/import` (base URL `https://telemetry.betterstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-dashboard.md) for the provider-specific parameters and requirements.

