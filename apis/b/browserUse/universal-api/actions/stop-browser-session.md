# Browser Use: Stop Browser Session

Stops a browser session in Browser Use.

```
PUT https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/stop-browser-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browser Use `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/stop-browser-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "stop",
  "sessionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/stop-browser-session', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "stop",
    "sessionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `action` | list | yes | Browser session update action. Use stop. One of: `0`. Default: `stop`. |
| `sessionId` | string | yes | Browser session ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `finishedAt` | date |  |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Browser Use API, this operation is `PATCH /browsers/:session_id` (base URL `https://api.browser-use.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stop-browser-session.md) for the provider-specific parameters and requirements.

