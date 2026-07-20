# Sempico Solutions SMS: Send SMS



```
POST https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/send-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sempico Solutions SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/send-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "number[]": [
    "string"
  ],
  "senderID": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sempicoSolutionsSMS/latest/actions/send-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "number[]": ["string"],
    "senderID": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `number[]` | array<string> | yes | Destination phone numbers in MSISDN format. |
| `senderID` | string | yes | Registered sender ID from which the SMS will be sent. Sempico rejects unregistered sender IDs with not_registr_originator. |
| `text` | string | yes | SMS message text. |
| `type` | list | no | Message type. Sempico documents sms, hlr, and mnp; defaults to sms. One of: `0`, `1`, `2`. Default: `sms`. |
| `delivery` | boolean | no | Whether Sempico should return delivery report information. Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `beginDate` | date | no | Date when the message should be sent, in YYYY-MM-DD format. |
| `beginTime` | string | no | GMT+0 time when the message should be sent, in HH:MM:SS format. |
| `lifetime` | number | no | How many seconds the SMS should live before expiring. Default: `86400`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sending": {
        "details": {
          "number": [
            "string"
          ],
          "senderID": "string",
          "sentID": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sending.details.number` | array<string> | Recipient phone numbers accepted by Sempico. |
| `sending.details.senderID` | string | Sender ID used for the message. |
| `sending.details.sentID` | number | Sempico sent SMS ID when a message is accepted. |

## Native endpoint

Through the native Sempico Solutions SMS API, this operation is `POST /send` (base URL `https://restapi.sempico.solutions/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms.md) for the provider-specific parameters and requirements.

