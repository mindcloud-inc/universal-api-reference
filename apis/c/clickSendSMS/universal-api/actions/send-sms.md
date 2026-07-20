# ClickSend SMS: Send SMS

Creates a new SMS message in ClickSend SMS.

```
POST https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/send-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/send-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messages[]": [
    {}
  ],
  "messages[].to": "string",
  "messages[].body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/send-sms', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messages[]": [{}],
    "messages[].to": "string",
    "messages[].body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messages[]` | array<object> | yes | Array payload for /v3/sms/send. Each object includes required to and body fields plus optional source, from, schedule, custom_string, and country. |
| `messages[].to` | string | yes | Destination phone number in international format. |
| `messages[].body` | string | yes | SMS content text. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messages[].from` | string | no | Sender ID or originating number where supported. |
| `messages[].source` | string | no | Source identifier, for example 'sdk'. Default: `sdk`. |
| `messages[].schedule` | string | no | Scheduled send time where supported by provider format. |
| `messages[].customString` | string | no | Custom tracking metadata string. |
| `messages[].country` | string | no | Country code override for destination handling. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blockedCount": 1,
      "currency": {
        "currencyNameLong": "Ava Chen",
        "currencyNameShort": "Ava Chen",
        "currencyPrefixC": "string",
        "currencyPrefixD": "string"
      },
      "messages": [
        {
          "body": "string",
          "isSharedSystemNumber": true,
          "messageId": "string",
          "status": "string"
        }
      ],
      "queuedCount": 1,
      "totalCount": 1,
      "totalPrice": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blockedCount` | number |  |
| `currency.currencyNameLong` | string |  |
| `currency.currencyNameShort` | string |  |
| `currency.currencyPrefixC` | string |  |
| `currency.currencyPrefixD` | string |  |
| `messages[].body` | string |  |
| `messages[].isSharedSystemNumber` | boolean |  |
| `messages[].messageId` | string |  |
| `messages[].status` | string |  |
| `queuedCount` | number |  |
| `totalCount` | number |  |
| `totalPrice` | number |  |

## Native endpoint

Through the native ClickSend SMS API, this operation is `POST /v3/sms/send` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms.md) for the provider-specific parameters and requirements.

