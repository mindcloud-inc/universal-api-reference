# Datadog: Validate Monitor

Validates a monitor configuration in Datadog.

```
GET https://connect.mindcloud.co/v1/universal/datadog/latest/actions/validate-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/validate-monitor?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datadog/latest/actions/validate-monitor?${params}`, {
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
| `message` | string | no | Notification message to validate. |
| `name` | string | no | Human-readable monitor name to validate. |
| `options` | object | no | Monitor options object to validate. |
| `priority` | number | no | Alert severity from 1 (high) to 5 (low). |
| `query` | string | yes | Monitor query expression to validate. |
| `restrictedRoles[]` | array<string> | no | Role IDs allowed to edit the monitor. |
| `tags[]` | array<string> | no | Tags associated with the monitor. |
| `type` | string | no | Datadog monitor type. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Datadog API returns.

## Native endpoint

Through the native Datadog API, this operation is `POST /api/v1/monitor/validate` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-monitor.md) for the provider-specific parameters and requirements.

