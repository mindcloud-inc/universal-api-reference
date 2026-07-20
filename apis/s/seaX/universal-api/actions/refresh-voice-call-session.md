# SeaX: Refresh Voice Call Session

Updates voice call session statistics in SeaX.

```
PUT https://connect.mindcloud.co/v1/universal/seaX/latest/actions/refresh-voice-call-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/refresh-voice-call-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaX/latest/actions/refresh-voice-call-session', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "call_sid": "string",
      "created_time": "string",
      "direction": {},
      "from_number": "string",
      "id": "string",
      "phone_id": "string",
      "stream_sid": "string",
      "to_number": "string",
      "total_duration": 1,
      "type": {},
      "updated_time": "string",
      "workspace_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `call_sid` | string |  |
| `created_time` | string |  |
| `direction` | object |  |
| `from_number` | string |  |
| `id` | string |  |
| `phone_id` | string |  |
| `stream_sid` | string |  |
| `to_number` | string |  |
| `total_duration` | number |  |
| `type` | object |  |
| `updated_time` | string |  |
| `workspace_id` | string |  |

## Native endpoint

Through the native SeaX API, this operation is `POST /voice_call_sessions/{session_id}/refresh` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refresh-voice-call-session.md) for the provider-specific parameters and requirements.

