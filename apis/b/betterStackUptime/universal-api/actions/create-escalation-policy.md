# Better Stack Uptime: Create Escalation Policy

Creates a new escalation policy in Better Stack Uptime.

```
POST https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/create-escalation-policy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Uptime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/create-escalation-policy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "steps[0].wait_before": "0",
  "steps[0].instructions_comment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/create-escalation-policy', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "steps[0].wait_before": "0",
    "steps[0].instructions_comment": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Escalation policy name. |
| `steps[0].wait_before` | number | yes | Seconds to wait before running the first step. Default: `0`. |
| `steps[0].instructions_comment` | string | yes | Instructions text for the first step. |
| `steps[0].instructions_reminder_enabled` | boolean | no | Whether to keep reminding for the instruction step. Default: `false`. |
| `teamName` | string | no | Better Stack team name when required by the token scope. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Uptime API returns.

## Native endpoint

Through the native Better Stack Uptime API, this operation is `POST /v3/policies` (base URL `https://uptime.betterstack.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-escalation-policy.md) for the provider-specific parameters and requirements.

