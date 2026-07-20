# Bento Now: Run Subscriber Command

Runs a targeted subscriber command in Bento Now.

```
PUT https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/run-subscriber-command
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bento Now `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/run-subscriber-command" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "command.command": "string",
  "command.email": "ava@example.com",
  "command.query": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bentoNow/latest/actions/run-subscriber-command', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "command.command": "string",
    "command.email": "ava@example.com",
    "command.query": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `command.command` | string | yes |  |
| `command.email` | string | yes |  |
| `command.query` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | number |  |

## Native endpoint

Through the native Bento Now API, this operation is `POST /v1/fetch/commands` (base URL `https://app.bentonow.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-subscriber-command.md) for the provider-specific parameters and requirements.

