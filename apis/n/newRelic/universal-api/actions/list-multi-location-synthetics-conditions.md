# New Relic: List Multi-Location Synthetics Conditions

Retrieves multi-location synthetics conditions from New Relic.

```
GET https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-multi-location-synthetics-conditions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-multi-location-synthetics-conditions?connectionId=$CONNECTION_ID&policyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "policyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-multi-location-synthetics-conditions?${params}`, {
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
| `policyId` | number | yes | New Relic alert policy ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "location_failure_conditions": [
        {
          "enabled": true,
          "entities": [
            [
              1
            ]
          ],
          "id": 1,
          "monitor_id": "string",
          "name": "Ava Chen",
          "runbook_url": "https://example.com"
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
| `location_failure_conditions[].enabled` | boolean |  |
| `location_failure_conditions[].entities[]` | array<number> |  |
| `location_failure_conditions[].id` | number |  |
| `location_failure_conditions[].monitor_id` | string |  |
| `location_failure_conditions[].name` | string |  |
| `location_failure_conditions[].runbook_url` | string |  |

## Native endpoint

Through the native New Relic API, this operation is `GET /alerts_location_failure_conditions/policies/:policyId.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-multi-location-synthetics-conditions.md) for the provider-specific parameters and requirements.

