# Datadog: List Monitors

Retrieves monitors from Datadog.

```
GET https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-monitors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-monitors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-monitors?${params}`, {
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
| `groupStates` | string | no | Comma-separated monitor group states to include: all, alert, warn, or no data. |
| `monitorTags` | string | no | Comma-separated service or custom monitor tags to filter the monitor list. |
| `name` | string | no | Filter monitors by monitor name. |
| `page` | number | no | Page number to start paginating from. |
| `pageSize` | number | no | Number of monitors to return per page. |
| `tags` | string | no | Comma-separated scope tags to filter the monitor list. |
| `withDowntimes` | boolean | no | Include current active downtimes for each returned monitor. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `idOffset` | number | no | Starting monitor ID for offset-style pagination through large monitor sets. |

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

Through the native Datadog API, this operation is `GET /api/v1/monitor` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-monitors.md) for the provider-specific parameters and requirements.

