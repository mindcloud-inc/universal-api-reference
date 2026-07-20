# Better Stack Telemetry: Get Dashboard

Retrieves a dashboard from Better Stack Telemetry.

```
GET https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/get-dashboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Telemetry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/get-dashboard?connectionId=$CONNECTION_ID&id=1234" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1234"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/get-dashboard?${params}`, {
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
| `id` | string | yes | The unique identifier of the dashboard. Example: `1234`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Telemetry API returns.

## Native endpoint

Through the native Better Stack Telemetry API, this operation is `GET /api/v2/dashboards/:id` (base URL `https://telemetry.betterstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dashboard.md) for the provider-specific parameters and requirements.

