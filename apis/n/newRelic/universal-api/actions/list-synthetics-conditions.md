# New Relic: List Synthetics Conditions

Retrieves synthetics conditions from New Relic.

```
GET https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-synthetics-conditions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-synthetics-conditions?connectionId=$CONNECTION_ID&policyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "policyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/list-synthetics-conditions?${params}`, {
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
| `policyId` | number | yes | Filter synthetics conditions by alert policy ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "synthetics_conditions": [
        {
          "enabled": true,
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
| `synthetics_conditions[].enabled` | boolean |  |
| `synthetics_conditions[].id` | number |  |
| `synthetics_conditions[].monitor_id` | string |  |
| `synthetics_conditions[].name` | string |  |
| `synthetics_conditions[].runbook_url` | string |  |

## Native endpoint

Through the native New Relic API, this operation is `GET /alerts_synthetics_conditions.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-synthetics-conditions.md) for the provider-specific parameters and requirements.

