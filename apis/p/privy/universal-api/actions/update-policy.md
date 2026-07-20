# Privy: Update Policy

Updates an existing policy in Privy.

```
PUT https://connect.mindcloud.co/v1/universal/privy/latest/actions/update-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/privy/latest/actions/update-policy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "policyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/privy/latest/actions/update-policy', {
  method: 'PUT',
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
      "chain_type": "string",
      "created_at": 1,
      "id": "string",
      "name": "Ava Chen",
      "owner_id": "string",
      "rules": [
        {
          "action": "string",
          "id": "string",
          "method": "string",
          "name": "Ava Chen"
        }
      ],
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chain_type` | string |  |
| `created_at` | number |  |
| `id` | string |  |
| `name` | string |  |
| `owner_id` | string |  |
| `rules[].action` | string |  |
| `rules[].id` | string |  |
| `rules[].method` | string |  |
| `rules[].name` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Privy API, this operation is `PATCH /v1/policies/{{policyId}}` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-policy.md) for the provider-specific parameters and requirements.

