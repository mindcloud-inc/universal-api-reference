# Mocean API: Send Binary SMS



```
POST https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/send-binary-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mocean API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/send-binary-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "hexPayload": "string",
  "recipient": "string",
  "sender": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moceanAPI/latest/actions/send-binary-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "hexPayload": "string",
    "recipient": "string",
    "sender": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hexPayload` | string | yes | Hex-encoded SMS payload. |
| `recipient` | string | yes | Recipient phone number with country code. |
| `sender` | string | yes | SMS sender ID. |
| `udh` | string | no | Optional user data header hex string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errMsg": "string",
      "messages": [
        {
          "errMsg": "string",
          "msgid": "string",
          "receiver": "string",
          "status": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errMsg` | string |  |
| `messages` | array<object> |  |
| `messages[].errMsg` | string |  |
| `messages[].msgid` | string |  |
| `messages[].receiver` | string |  |
| `messages[].status` | number |  |

## Native endpoint

Through the native Mocean API API, this operation is `POST /rest/2/sms?mocean-resp-format=json&mocean-coding=2` (base URL `https://rest.moceanapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-binary-sms.md) for the provider-specific parameters and requirements.

