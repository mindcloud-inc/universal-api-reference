# Dialpad: Get Call Transcript

Retrieves a Dialpad AI transcript for a call.

```
GET https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/get-call-transcript
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/get-call-transcript?connectionId=$CONNECTION_ID&call_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "call_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/get-call-transcript?${params}`, {
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
| `call_id` | number | yes | The call's id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callId": "string",
      "lines": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callId` | string | The call ID. |
| `lines` | array<object> | Transcript lines for the call. |

## Native endpoint

Through the native Dialpad API, this operation is `GET /transcripts/:call_id` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-call-transcript.md) for the provider-specific parameters and requirements.

