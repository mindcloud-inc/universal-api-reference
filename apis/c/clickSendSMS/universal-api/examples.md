# ClickSend SMS Universal API Examples

These examples use the MindCloud API key and ClickSend SMS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Calculate SMS Campaign Price

Calculates SMS campaign pricing in ClickSend SMS.

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

Example response:

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

See the full [Calculate SMS Campaign Price action reference](actions/calculate-sms-campaign-price.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clickSendSMS/latest/actions/calculate-sms-campaign-price).

## Cancel SMS

Cancels an SMS message in ClickSend SMS.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/cancel-sms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "message_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clickSendSMS/latest/actions/cancel-sms', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "message_id": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "httpCode": "string",
      "responseCode": "string",
      "responseMsg": "string"
    }
  ],
  "meta": {}
}
```

See the full [Cancel SMS action reference](actions/cancel-sms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/clickSendSMS/latest/actions/cancel-sms).
