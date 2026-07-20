# New Relic: Update NRQL Condition

Updates an existing NRQL condition in New Relic.

```
PUT https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/update-nrql-condition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/update-nrql-condition" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conditionId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/update-nrql-condition', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conditionId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conditionId` | number | yes | New Relic alert condition ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nrql_condition": {
        "enabled": true,
        "expected_groups": 1,
        "id": 1,
        "ignore_overlap": true,
        "name": "Ava Chen",
        "nrql": {
          "query": "string",
          "since_value": "string"
        },
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
        "value_function": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nrql_condition.enabled` | boolean |  |
| `nrql_condition.expected_groups` | number |  |
| `nrql_condition.id` | number |  |
| `nrql_condition.ignore_overlap` | boolean |  |
| `nrql_condition.name` | string |  |
| `nrql_condition.nrql.query` | string |  |
| `nrql_condition.nrql.since_value` | string |  |
| `nrql_condition.runbook_url` | string |  |
| `nrql_condition.terms[].duration` | string |  |
| `nrql_condition.terms[].operator` | string |  |
| `nrql_condition.terms[].priority` | string |  |
| `nrql_condition.terms[].threshold` | string |  |
| `nrql_condition.terms[].time_function` | string |  |
| `nrql_condition.type` | string |  |
| `nrql_condition.value_function` | string |  |

## Native endpoint

Through the native New Relic API, this operation is `PUT /alerts_nrql_conditions/:conditionId.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-nrql-condition.md) for the provider-specific parameters and requirements.

