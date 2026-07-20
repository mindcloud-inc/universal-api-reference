# Datadog: Get Monitor Details

Retrieves monitor details from Datadog.

```
GET https://connect.mindcloud.co/v1/universal/datadog/latest/actions/get-monitor-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/get-monitor-details?connectionId=$CONNECTION_ID&monitorId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "monitorId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datadog/latest/actions/get-monitor-details?${params}`, {
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
| `monitorId` | number | yes | The ID of the monitor to retrieve. |
| `withAssets` | boolean | no | Include assets tied to the monitor in the returned response. |
| `withDowntimes` | boolean | no | Include current active downtimes for the monitor in the returned response. |

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

Through the native Datadog API, this operation is `GET /api/v1/monitor/:monitor_id` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-monitor-details.md) for the provider-specific parameters and requirements.

