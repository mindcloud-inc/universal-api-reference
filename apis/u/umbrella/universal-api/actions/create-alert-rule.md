# Umbrella: Create Alert Rule

Creates a new alert rule in Umbrella.

```
POST https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/create-alert-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbrella `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/create-alert-rule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "severity": 1,
  "status": 1,
  "rule_type_id": 1,
  "notification_info.0.type": "string",
  "notification_info.0.recipients.0": "string",
  "conditions.match_type": "string",
  "conditions.rows.0.field": "string",
  "conditions.rows.0.value": "string",
  "conditions.rows.1.field": "string",
  "conditions.rows.1.value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/umbrella/latest/actions/create-alert-rule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "severity": 1,
    "status": 1,
    "rule_type_id": 1,
    "notification_info.0.type": "string",
    "notification_info.0.recipients.0": "string",
    "conditions.match_type": "string",
    "conditions.rows.0.field": "string",
    "conditions.rows.0.value": "string",
    "conditions.rows.1.field": "string",
    "conditions.rows.1.value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Short description for the alert rule. |
| `name` | string | yes | The alert rule name. |
| `severity` | number | yes | 1 High, 2 Medium, 3 Low, 4 Info. |
| `status` | number | yes | 1 enabled, 2 disabled. |
| `rule_type_id` | number | yes | The alert rule type ID. |
| `notification_info.0.type` | string | yes | email or webhook. |
| `notification_info.0.recipients.0` | string | yes | First email recipient. |
| `conditions.match_type` | string | yes | all or any. |
| `conditions.rows.0.field` | string | yes | First condition field. |
| `conditions.rows.0.value` | string | yes | First condition value. |
| `conditions.rows.1.field` | string | yes | Second condition field. |
| `conditions.rows.1.value` | string | yes | Second condition value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Umbrella API, this operation is `POST https://api.sse.cisco.com/admin/v2/alerting/rules` (base URL `https://api.umbrella.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-alert-rule.md) for the provider-specific parameters and requirements.

