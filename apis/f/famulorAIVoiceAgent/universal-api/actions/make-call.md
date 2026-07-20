# Famulor AI - Voice Agent: Make a Call

Creates a new call in Famulor with a specific assistant.

```
POST https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/make-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Famulor AI - Voice Agent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/make-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assistant_id": 1,
  "phone_number": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/famulorAIVoiceAgent/latest/actions/make-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assistant_id": 1,
    "phone_number": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assistant_id` | number | yes | Assistant ID that will handle the call. |
| `phone_number` | string | yes | Destination phone number in E.164 format. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables` | object | no | Optional dynamic variables for call personalization. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "call_id": 1,
      "data": {},
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `call_id` | number | Created call ID. |
| `data` | object | Call metadata. |
| `message` | string | Result message. |
| `status` | string | Initial call status. |

## Native endpoint

Through the native Famulor AI - Voice Agent API, this operation is `POST /user/make_call` (base URL `https://app.famulor.de/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/make-call.md) for the provider-specific parameters and requirements.

