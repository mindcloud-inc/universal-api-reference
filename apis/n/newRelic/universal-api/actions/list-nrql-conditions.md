# New Relic: List NRQL Conditions

Retrieves NRQL conditions from New Relic.

```
GET https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-nrql-conditions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-nrql-conditions?connectionId=$CONNECTION_ID&policyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "policyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-nrql-conditions?${params}`, {
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
| `policyId` | number | yes | Filter NRQL conditions by alert policy ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nrql_conditions": [
        {
          "enabled": true,
          "id": 1,
          "name": "Ava Chen",
          "nrql": {
            "query": "string"
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
          ]
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
| `nrql_conditions[].enabled` | boolean |  |
| `nrql_conditions[].id` | number |  |
| `nrql_conditions[].name` | string |  |
| `nrql_conditions[].nrql.query` | string |  |
| `nrql_conditions[].runbook_url` | string |  |
| `nrql_conditions[].terms[].duration` | string |  |
| `nrql_conditions[].terms[].operator` | string |  |
| `nrql_conditions[].terms[].priority` | string |  |
| `nrql_conditions[].terms[].threshold` | string |  |
| `nrql_conditions[].terms[].time_function` | string |  |

## Native endpoint

Through the native New Relic API, this operation is `GET /alerts_nrql_conditions.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-nrql-conditions.md) for the provider-specific parameters and requirements.

