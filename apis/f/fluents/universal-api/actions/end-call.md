# Fluents: End Call

Ends an active call in Fluents.

```
PUT https://connect.mindcloud.co/v1/universal/fluents/latest/actions/end-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fluents/latest/actions/end-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fluents/latest/actions/end-call', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Fluents call ID to end. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent": {},
      "end_time": "string",
      "errors": [
        "string"
      ],
      "from_number": "string",
      "id": "string",
      "is_outgoing": true,
      "recording_available": true,
      "start_time": "string",
      "status": "string",
      "to_number": "string",
      "transcript": "string",
      "user_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent` | object |  |
| `end_time` | string |  |
| `errors` | array<string> |  |
| `from_number` | string |  |
| `id` | string |  |
| `is_outgoing` | boolean |  |
| `recording_available` | boolean |  |
| `start_time` | string |  |
| `status` | string |  |
| `to_number` | string |  |
| `transcript` | string |  |
| `user_id` | string |  |

## Native endpoint

Through the native Fluents API, this operation is `POST /calls/end` (base URL `https://api.fluents.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/end-call.md) for the provider-specific parameters and requirements.

