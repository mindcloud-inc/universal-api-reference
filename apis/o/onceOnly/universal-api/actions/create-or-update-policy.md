# OnceOnly: Create or Update Policy

Creates or updates a policy in OnceOnly.

```
PUT https://connect.mindcloud.co/v1/universal/onceOnly/latest/actions/create-or-update-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnceOnly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/onceOnly/latest/actions/create-or-update-policy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onceOnly/latest/actions/create-or-update-policy', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | Agent id to update policy for. |
| `allowedTools[]` | array<string> | no | Allowed tool names. |
| `blockedTools[]` | array<string> | no | Blocked tool names. |
| `maxActionsPerHour` | number | no | Hourly action cap. |
| `maxSpendUsdPerDay` | number | no | Daily spend cap in USD. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native OnceOnly API returns.

## Native endpoint

Through the native OnceOnly API, this operation is `POST /v1/policies/:agent_id` (base URL `https://api.onceonly.tech`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-policy.md) for the provider-specific parameters and requirements.

