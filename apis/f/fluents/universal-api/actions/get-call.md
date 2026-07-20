# Fluents: Get Call

Retrieves a call from your Fluents account.

```
GET https://connect.mindcloud.co/v1/universal/fluents/latest/actions/get-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fluents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fluents/latest/actions/get-call?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fluents/latest/actions/get-call?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Fluents call ID. |

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

Through the native Fluents API, this operation is `GET /calls` (base URL `https://api.fluents.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call.md) for the provider-specific parameters and requirements.

