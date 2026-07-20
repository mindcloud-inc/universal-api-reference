# Browser Use: Stop Session

Stops a session or running task in Browser Use.

```
PUT https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/stop-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Browser Use `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/stop-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/browserUse/latest/actions/stop-session', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | yes | Browser Use session ID. |
| `strategy` | list | no | Stop strategy: task or session. One of: `0`, `1`. Default: `session`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "isTaskSuccessful": true,
      "status": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `isTaskSuccessful` | boolean |  |
| `status` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Browser Use API, this operation is `POST /sessions/:session_id/stop` (base URL `https://api.browser-use.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stop-session.md) for the provider-specific parameters and requirements.

