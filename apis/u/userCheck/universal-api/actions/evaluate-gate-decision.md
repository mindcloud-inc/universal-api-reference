# UserCheck: Evaluate Gate Decision

Requests a gate decision from UserCheck.

```
POST https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/evaluate-gate-decision
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserCheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/evaluate-gate-decision" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "gateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userCheck/latest/actions/evaluate-gate-decision', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "gateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `gateId` | string | yes | Gate identifier from the UserCheck dashboard. |
| `email` | string | no | Email address to evaluate. Provide either Email or Domain. |
| `domain` | string | no | Domain to evaluate. Provide either Domain or Email. |
| `ip` | string | no | Optional IP address for additional intelligence. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "decision": {},
      "input": {},
      "meta": {},
      "signals": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `decision` | object |  |
| `input` | object |  |
| `meta` | object |  |
| `signals` | object |  |

## Native endpoint

Through the native UserCheck API, this operation is `POST /v0/gates/:gateId/decisions` (base URL `https://api.usercheck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/evaluate-gate-decision.md) for the provider-specific parameters and requirements.

