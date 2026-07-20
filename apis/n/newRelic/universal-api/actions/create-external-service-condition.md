# New Relic: Create External Service Condition

Creates a new external service condition in New Relic.

```
POST https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/create-external-service-condition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/create-external-service-condition" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "policyId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/create-external-service-condition', {
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
      "external_service_condition": {
        "enabled": true,
        "entities": [
          1
        ],
        "external_service_url": "https://example.com",
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
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `external_service_condition.enabled` | boolean |  |
| `external_service_condition.entities[]` | number |  |
| `external_service_condition.external_service_url` | string |  |
| `external_service_condition.id` | number |  |
| `external_service_condition.metric` | string |  |
| `external_service_condition.name` | string |  |
| `external_service_condition.runbook_url` | string |  |
| `external_service_condition.terms[].duration` | string |  |
| `external_service_condition.terms[].operator` | string |  |
| `external_service_condition.terms[].priority` | string |  |
| `external_service_condition.terms[].threshold` | string |  |
| `external_service_condition.terms[].time_function` | string |  |
| `external_service_condition.type` | string |  |

## Native endpoint

Through the native New Relic API, this operation is `POST /alerts_external_service_conditions/policies/:policyId.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-external-service-condition.md) for the provider-specific parameters and requirements.

