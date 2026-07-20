# Umbrella: List Active High Severity Alerts

Retrieves active high-severity alerts from Umbrella.

```
GET https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/list-active-high-severity-alerts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbrella `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/list-active-high-severity-alerts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/list-active-high-severity-alerts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "alertId": "string",
      "context": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "modified_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "organization_id": 1,
      "rule_id": 1,
      "rule_type_id": 1,
      "severity": 1,
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alertId` | string |  |
| `context` | object |  |
| `created_at` | date |  |
| `description` | string |  |
| `modified_at` | date |  |
| `name` | string |  |
| `organization_id` | number |  |
| `rule_id` | number |  |
| `rule_type_id` | number |  |
| `severity` | number |  |
| `status` | number |  |

## Native endpoint

Through the native Umbrella API, this operation is `GET https://api.sse.cisco.com/admin/v2/alerting/alerts?filters={"status":1,"severity":1}` (base URL `https://api.umbrella.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-active-high-severity-alerts.md) for the provider-specific parameters and requirements.

