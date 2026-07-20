# Agenthost.ai: Log In

Starts or completes Agenthost.ai login by email verification.

```
POST https://connect.mindcloud.co/v1/universal/agenthostai/latest/actions/log-in
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agenthost.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agenthostai/latest/actions/log-in" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "user@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agenthostai/latest/actions/log-in', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "user@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The user's email address. Example: `user@example.com`. |
| `code` | string | no | Code sent to the user's email. Example: `123456`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agenthost.ai API returns.

## Native endpoint

Through the native Agenthost.ai API, this operation is `POST /api/openai/log_in/` (base URL `https://api.agenthost.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/log-in.md) for the provider-specific parameters and requirements.

