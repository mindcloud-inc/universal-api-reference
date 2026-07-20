# VoiceShot: Send Per-Recipient SMS Batch

Creates per-recipient SMS messages in VoiceShot.

```
POST https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/send-per-recipient-sms-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VoiceShot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/send-per-recipient-sms-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "menuId": "string",
  "recipients[]": [
    {}
  ],
  "recipients[].number": "string",
  "recipients[].message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceShot/latest/actions/send-per-recipient-sms-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "menuId": "string",
    "recipients[]": [{}],
    "recipients[].number": "string",
    "recipients[].message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `menuId` | string | yes | VoiceShot campaign identifier. |
| `recipients[]` | array<object> | yes | Recipient list with per-recipient SMS content. |
| `recipients[].number` | string | yes | Destination phone number. |
| `recipients[].message` | string | yes | SMS body for this recipient. |
| `recipients[].callId` | string | no | Optional client-defined call identifier. |
| `recipients[].callerId` | string | no | Optional caller ID for this recipient. |
| `recipients[].countryCode` | string | no | Optional country code. |
| `recipients[].dateAndTime` | string | no | Optional scheduled delivery time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": "string",
      "errorId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | string | VoiceShot response comment or error message. |
| `errorId` | string | VoiceShot response error code. 0 means ok. |

## Native endpoint

Through the native VoiceShot API, this operation is `POST /ivrapi.asp` (base URL `https://api.voiceshot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-per-recipient-sms-batch.md) for the provider-specific parameters and requirements.

