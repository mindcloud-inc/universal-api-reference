# New Relic: Create Alert Policy

Creates a new alert policy in New Relic.

```
POST https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/create-alert-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/create-alert-policy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "incidentPreference": "PER_POLICY"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/create-alert-policy', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "incidentPreference": "PER_POLICY"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Alert policy name. |
| `incidentPreference` | list | yes | How incidents are grouped for this policy. One of: `0`, `1`, `2`. Default: `PER_POLICY`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "policy": {
        "created_at": 1,
        "id": 1,
        "incident_preference": "string",
        "name": "Ava Chen",
        "updated_at": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `policy.created_at` | number |  |
| `policy.id` | number |  |
| `policy.incident_preference` | string |  |
| `policy.name` | string |  |
| `policy.updated_at` | number |  |

## Native endpoint

Through the native New Relic API, this operation is `POST /alerts_policies.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-alert-policy.md) for the provider-specific parameters and requirements.

