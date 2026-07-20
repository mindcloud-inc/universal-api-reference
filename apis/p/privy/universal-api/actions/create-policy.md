# Privy: Create Policy

Creates a new policy in Privy.

```
POST https://connect.mindcloud.co/v1/universal/privy/latest/actions/create-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/privy/latest/actions/create-policy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/privy/latest/actions/create-policy', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



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

Through the native Privy API, this operation is `POST /v1/policies` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-policy.md) for the provider-specific parameters and requirements.

