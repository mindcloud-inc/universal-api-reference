# New Relic: Create Synthetics Condition

Creates a new synthetics condition in New Relic.

```
POST https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/create-synthetics-condition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/create-synthetics-condition" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "policyId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/create-synthetics-condition', {
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
      "synthetics_condition": {
        "enabled": true,
        "id": 1,
        "monitor_id": "string",
        "name": "Ava Chen",
        "runbook_url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `synthetics_condition.enabled` | boolean |  |
| `synthetics_condition.id` | number |  |
| `synthetics_condition.monitor_id` | string |  |
| `synthetics_condition.name` | string |  |
| `synthetics_condition.runbook_url` | string |  |

## Native endpoint

Through the native New Relic API, this operation is `POST /alerts_synthetics_conditions/policies/:policyId.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-synthetics-condition.md) for the provider-specific parameters and requirements.

