# Privy: Create Policy Rule

Creates a new rule for a Privy policy.

```
POST https://connect.mindcloud.co/v1/universal/privy/latest/actions/create-policy-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/privy/latest/actions/create-policy-rule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "policyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/privy/latest/actions/create-policy-rule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "policyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `policyId` | string | yes | Privy policy ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "conditions": [
        {
          "field": "string",
          "field_source": "string",
          "operator": "string",
          "value": "string"
        }
      ],
      "id": "string",
      "method": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `conditions[].field` | string |  |
| `conditions[].field_source` | string |  |
| `conditions[].operator` | string |  |
| `conditions[].value` | string |  |
| `id` | string |  |
| `method` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Privy API, this operation is `POST /v1/policies/{{policyId}}/rules` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-policy-rule.md) for the provider-specific parameters and requirements.

