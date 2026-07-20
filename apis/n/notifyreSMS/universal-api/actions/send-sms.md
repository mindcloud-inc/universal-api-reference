# Notifyre SMS: Send SMS

Creates an SMS message in Notifyre.

```
POST https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/send-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notifyre SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/send-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "string",
  "from": "string",
  "recipients": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notifyreSMS/latest/actions/send-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "string",
    "from": "string",
    "recipients": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | yes | SMS message body. |
| `campaignName` | string | no | Optional campaign label. |
| `from` | string | yes | Sending number or sender ID. |
| `recipients` | list<string> | yes | Recipient phone numbers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "friendlyID": "string",
      "invalidToNumbers": [
        {}
      ],
      "smsMessageID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `friendlyID` | string | Human-friendly reference for the SMS message. |
| `invalidToNumbers` | array<object> | Rejected recipient numbers, if any. |
| `smsMessageID` | string | Identifier of the created SMS message. |

## Native endpoint

Through the native Notifyre SMS API, this operation is `POST /sms/send` (base URL `https://api.notifyre.com/20220711`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms.md) for the provider-specific parameters and requirements.

