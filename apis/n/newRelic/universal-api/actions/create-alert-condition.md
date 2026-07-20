# New Relic: Create Alert Condition

Creates a new alert condition in New Relic.

```
POST https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/create-alert-condition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/create-alert-condition" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "policyId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/create-alert-condition', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "policyId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `policyId` | number | yes | New Relic alert policy ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "condition": {
        "condition_scope": "string",
        "enabled": true,
        "entities": [
          1
        ],
        "id": 1,
        "metric": "string",
        "name": "Ava Chen",
        "runbook_url": "https://example.com",
        "terms": [
          {
            "duration": "string",
            "operator": "string",
            "priority": "string",
            "threshold": "string",
            "time_function": "string"
          }
        ],
        "type": "string",
        "violation_close_timer": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `condition.condition_scope` | string |  |
| `condition.enabled` | boolean |  |
| `condition.entities[]` | number |  |
| `condition.id` | number |  |
| `condition.metric` | string |  |
| `condition.name` | string |  |
| `condition.runbook_url` | string |  |
| `condition.terms[].duration` | string |  |
| `condition.terms[].operator` | string |  |
| `condition.terms[].priority` | string |  |
| `condition.terms[].threshold` | string |  |
| `condition.terms[].time_function` | string |  |
| `condition.type` | string |  |
| `condition.violation_close_timer` | number |  |

## Native endpoint

Through the native New Relic API, this operation is `POST /alerts_conditions/policies/:policyId.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-alert-condition.md) for the provider-specific parameters and requirements.

