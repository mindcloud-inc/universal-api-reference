# ClickSend SMS: Calculate SMS Price

Calculates SMS pricing in ClickSend SMS.

```
GET https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/calculate-sms-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/calculate-sms-price?connectionId=$CONNECTION_ID&messages%5B%5D=%5Bobject%20Object%5D&messages%5B%5D.to=string&messages%5B%5D.body=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messages[]": "[object Object]",
  "messages[].to": "string",
  "messages[].body": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/calculate-sms-price?${params}`, {
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
| `messages[]` | array<object> | yes | Array payload for /v3/sms/price. Each object includes required to and body plus optional source, from, schedule, custom_string, and country. |
| `messages[].to` | string | yes | Destination phone number in international format. |
| `messages[].body` | string | yes | SMS content text used for pricing. |

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

Through the native ClickSend SMS API, this operation is `POST /v3/sms/price` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-sms-price.md) for the provider-specific parameters and requirements.

