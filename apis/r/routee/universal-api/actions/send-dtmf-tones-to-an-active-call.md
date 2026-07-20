# Routee: Send DTMF tones to an active call

Sends DTMF tones to an active call with Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-dtmf-tones-to-an-active-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-dtmf-tones-to-an-active-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "string",
  "dtmf": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-dtmf-tones-to-an-active-call', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "string",
    "dtmf": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | yes | The id of the voice call |
| `dtmf` | string | yes | A string with the dtmf tones to be sent. Valid characters are given by the regular expression: [A-D0-9#*,wW]+. The ',' and lowercase 'w' characters represents a half-second pause into the DTMF sequence, while the uppercase 'W' character represents one-second pause. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "message": "string",
      "messageId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `message` | string |  |
| `messageId` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /voice/conversation/:messageId/dtmf` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-dtmf-tones-to-an-active-call.md) for the provider-specific parameters and requirements.

