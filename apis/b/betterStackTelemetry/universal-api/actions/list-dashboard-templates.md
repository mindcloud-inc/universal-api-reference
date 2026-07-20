# Better Stack Telemetry: List Dashboard Templates

Retrieves dashboard templates from Better Stack Telemetry.

```
GET https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/list-dashboard-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Telemetry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/list-dashboard-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/list-dashboard-templates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Telemetry API returns.

## Native endpoint

Through the native Better Stack Telemetry API, this operation is `GET /api/v2/dashboards/templates` (base URL `https://telemetry.betterstack.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dashboard-templates.md) for the provider-specific parameters and requirements.

