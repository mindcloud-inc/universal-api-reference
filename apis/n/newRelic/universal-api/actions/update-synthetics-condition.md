# New Relic: Update Synthetics Condition

Updates an existing synthetics condition in New Relic.

```
PUT https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/update-synthetics-condition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/update-synthetics-condition" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conditionId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/update-synthetics-condition', {
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

Through the native New Relic API, this operation is `PUT /alerts_synthetics_conditions/:conditionId.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-synthetics-condition.md) for the provider-specific parameters and requirements.

