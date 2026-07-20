# Better Stack Uptime: Create Incident

Creates a new incident in Better Stack Uptime.

```
POST https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/create-incident
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Uptime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/create-incident" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "summary": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/create-incident', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "summary": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `summary` | string | yes | Short incident summary shown in Better Stack. |
| `requesterEmail` | string | no | Email address of the incident reporter. |
| `description` | string | no | Detailed incident description. |
| `name` | string | no | Optional incident name. |
| `call` | boolean | no | Enable phone call notifications. Default: `false`. |
| `sms` | boolean | no | Enable SMS notifications. Default: `false`. |
| `email` | boolean | no | Enable email notifications. Default: `false`. |
| `criticalAlert` | boolean | no | Mark the incident as critical. Default: `false`. |
| `teamWait` | number | no | Seconds to wait before escalating to the team. |
| `policyId` | string | no | Escalation policy ID to apply to the incident. |
| `teamName` | string | no | Better Stack team name when required by the token scope. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Uptime API returns.

## Native endpoint

Through the native Better Stack Uptime API, this operation is `POST /v3/incidents` (base URL `https://uptime.betterstack.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-incident.md) for the provider-specific parameters and requirements.

