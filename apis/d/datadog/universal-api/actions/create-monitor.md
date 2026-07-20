# Datadog: Create Monitor

Creates a new monitor in Datadog.

```
POST https://connect.mindcloud.co/v1/universal/datadog/latest/actions/create-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/create-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datadog/latest/actions/create-monitor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | no | Notification message for the monitor. |
| `name` | string | no | Human-readable monitor name. |
| `options` | object | no | Monitor options object as documented by Datadog. |
| `priority` | number | no | Alert severity from 1 (high) to 5 (low). |
| `query` | string | yes | Monitor query expression. |
| `restrictedRoles[]` | array<string> | no | Role IDs allowed to edit the monitor. |
| `tags[]` | array<string> | no | Tags associated with the monitor. |
| `type` | string | no | Datadog monitor type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "creator": {},
      "draft_status": "string",
      "id": 1,
      "message": "string",
      "modified": "string",
      "name": "Ava Chen",
      "options": {},
      "org_id": 1,
      "overall_state": "string",
      "priority": 1,
      "query": "string",
      "restricted_roles": [
        "string"
      ],
      "tags": [
        "string"
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `creator` | object |  |
| `draft_status` | string |  |
| `id` | number |  |
| `message` | string |  |
| `modified` | string |  |
| `name` | string |  |
| `options` | object |  |
| `org_id` | number |  |
| `overall_state` | string |  |
| `priority` | number |  |
| `query` | string |  |
| `restricted_roles` | array<string> |  |
| `tags` | array<string> |  |
| `type` | string |  |

## Native endpoint

Through the native Datadog API, this operation is `POST /api/v1/monitor` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-monitor.md) for the provider-specific parameters and requirements.

