# New Relic: Delete Alert Policy

Deletes an existing alert policy from New Relic.

```
DELETE https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/delete-alert-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a New Relic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/delete-alert-policy?connectionId=$CONNECTION_ID&policyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "policyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/newRelic/latest/actions/delete-alert-policy?${params}`, {
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

Through the native New Relic API, this operation is `DELETE /alerts_policies/:policyId.json` (base URL `https://api.newrelic.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-alert-policy.md) for the provider-specific parameters and requirements.

