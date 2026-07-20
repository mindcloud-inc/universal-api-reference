# TRIGGERcmd: Trigger Command

Triggers a command on a computer in TRIGGERcmd.

```
POST https://connect.mindcloud.co/v1/universal/tRIGGERcmd/latest/actions/trigger-command
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TRIGGERcmd `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tRIGGERcmd/latest/actions/trigger-command" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "computer": "string",
  "trigger": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tRIGGERcmd/latest/actions/trigger-command', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "computer": "string",
    "trigger": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `computer` | string | yes | The computer name to target. |
| `trigger` | string | yes | The trigger name of the command to run. |
| `params` | string | no | Optional text to pass to the command. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TRIGGERcmd API returns.

## Native endpoint

Through the native TRIGGERcmd API, this operation is `POST /run/trigger` (base URL `https://www.triggercmd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/trigger-command.md) for the provider-specific parameters and requirements.

