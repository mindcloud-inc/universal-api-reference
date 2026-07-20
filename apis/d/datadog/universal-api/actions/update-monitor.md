# Datadog: Update Monitor

Updates an existing monitor in Datadog.

```
PUT https://connect.mindcloud.co/v1/universal/datadog/latest/actions/update-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/update-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "monitorId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datadog/latest/actions/update-monitor', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "monitorId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | no | Updated notification message. |
| `monitorId` | number | yes | The ID of the monitor to edit. |
| `name` | string | no | Updated monitor name. |
| `options` | object | no | Updated monitor options object. |
| `priority` | number | no | Updated alert severity from 1 (high) to 5 (low). |
| `query` | string | no | Updated monitor query expression. |
| `restrictedRoles[]` | array<string> | no | Updated role IDs allowed to edit the monitor. |
| `tags[]` | array<string> | no | Updated monitor tags. |
| `type` | string | no | Updated Datadog monitor type. |

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

Through the native Datadog API, this operation is `PUT /api/v1/monitor/:monitor_id` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-monitor.md) for the provider-specific parameters and requirements.

