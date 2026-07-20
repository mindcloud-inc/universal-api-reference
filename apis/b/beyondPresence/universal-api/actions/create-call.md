# Beyond Presence: Create Call

Creates a new call in Beyond Presence.

```
POST https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/create-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beyond Presence `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/create-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/create-call', {
  method: 'POST',
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
| `agentId` | string | yes | ID of agent managing the call. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "endedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "livekitToken": "string",
      "livekitUrl": "https://example.com",
      "startedAt": "2026-05-07T12:00:00.000Z",
      "tags": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string | ID of the agent managing the call. |
| `endedAt` | date | Call end time in ISO 8601 format when available. |
| `id` | string | Unique identifier of the call. |
| `livekitToken` | string | LiveKit token for joining the room. |
| `livekitUrl` | string | LiveKit server URL to connect to. |
| `startedAt` | date | Call start time in ISO 8601 format. |
| `tags` | object | Tags attached to the call. |

## Native endpoint

Through the native Beyond Presence API, this operation is `POST /v1/calls` (base URL `https://api.bey.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-call.md) for the provider-specific parameters and requirements.

