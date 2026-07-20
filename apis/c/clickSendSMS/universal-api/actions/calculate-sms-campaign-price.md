# ClickSend SMS: Calculate SMS Campaign Price

Calculates SMS campaign pricing in ClickSend SMS.

```
GET https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/calculate-sms-campaign-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickSend SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/calculate-sms-campaign-price?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/calculate-sms-campaign-price?${params}`, {
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
| `list_id` | string | no |  |
| `name` | string | no |  |
| `from` | string | no |  |
| `body` | string | no |  |

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
        "currencyPrefixD": "string",
        "maxRechargeAmount": "string",
        "minRechargeAmount": "string"
      },
      "data": {
        "body": {},
        "from": {},
        "schedule": 1
      },
      "totalCount": 1,
      "totalPrice": "string"
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
| `currency.maxRechargeAmount` | string |  |
| `currency.minRechargeAmount` | string |  |
| `data.body` | object |  |
| `data.from` | object |  |
| `data.schedule` | number |  |
| `totalCount` | number |  |
| `totalPrice` | string |  |

## Native endpoint

Through the native ClickSend SMS API, this operation is `POST /v3/sms-campaigns/price` (base URL `https://rest.clicksend.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-sms-campaign-price.md) for the provider-specific parameters and requirements.

