# New Relic: List External Service Conditions

Retrieves external service conditions from New Relic.

```
GET https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-external-service-conditions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-external-service-conditions?connectionId=$CONNECTION_ID&policyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "policyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-external-service-conditions?${params}`, {
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
| `policyId` | number | yes | Filter external service conditions by alert policy ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "external_service_conditions": [
        {
          "enabled": true,
          "entities": [
            [
              1
            ]
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
| `external_service_conditions[].enabled` | boolean |  |
| `external_service_conditions[].entities[]` | array<number> |  |
| `external_service_conditions[].external_service_url` | string |  |
| `external_service_conditions[].id` | number |  |
| `external_service_conditions[].metric` | string |  |
| `external_service_conditions[].name` | string |  |
| `external_service_conditions[].runbook_url` | string |  |
| `external_service_conditions[].terms[].duration` | string |  |
| `external_service_conditions[].terms[].operator` | string |  |
| `external_service_conditions[].terms[].priority` | string |  |
| `external_service_conditions[].terms[].threshold` | string |  |
| `external_service_conditions[].terms[].time_function` | string |  |

## Native endpoint

Through the native New Relic API, this operation is `GET /alerts_external_service_conditions.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-external-service-conditions.md) for the provider-specific parameters and requirements.

