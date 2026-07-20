# Voiceflow: Emit Session Event

Sends an event to an active Voiceflow session.

```
POST https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/emit-session-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/emit-session-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "mindcloud-vf-interact-user-001",
  "action": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/emit-session-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "mindcloud-vf-interact-user-001",
    "action": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | yes | Unique ID of the conversation session. Example: `mindcloud-vf-interact-user-001`. |
| `action` | object | yes | The event to send to the active conversation. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Voiceflow API returns.

## Native endpoint

Through the native Voiceflow API, this operation is `POST /v2/project/:projectId/session/:sessionId/event` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/emit-session-event.md) for the provider-specific parameters and requirements.

