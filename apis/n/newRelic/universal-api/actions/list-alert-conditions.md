# New Relic: List Alert Conditions

Retrieves alert conditions from New Relic.

```
GET https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-alert-conditions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-alert-conditions?connectionId=$CONNECTION_ID&policyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "policyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-alert-conditions?${params}`, {
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
| `policyId` | number | yes | Filter alert conditions by alert policy ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "conditions": [
        {
          "condition_scope": "string",
          "enabled": true,
          "entities": [
            [
              1
            ]
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `conditions[].condition_scope` | string |  |
| `conditions[].enabled` | boolean |  |
| `conditions[].entities[]` | array<number> |  |
| `conditions[].id` | number |  |
| `conditions[].metric` | string |  |
| `conditions[].name` | string |  |
| `conditions[].runbook_url` | string |  |
| `conditions[].terms[].duration` | string |  |
| `conditions[].terms[].operator` | string |  |
| `conditions[].terms[].priority` | string |  |
| `conditions[].terms[].threshold` | string |  |
| `conditions[].terms[].time_function` | string |  |
| `conditions[].type` | string |  |
| `conditions[].violation_close_timer` | number |  |

## Native endpoint

Through the native New Relic API, this operation is `GET /alerts_conditions.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alert-conditions.md) for the provider-specific parameters and requirements.

