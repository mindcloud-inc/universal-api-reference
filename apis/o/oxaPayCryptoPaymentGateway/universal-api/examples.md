# OxaPay Crypto Payment Gateway Universal API Examples

These examples use the MindCloud API key and OxaPay Crypto Payment Gateway connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Payments

Retrieves payments from OxaPay.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/list-payments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/list-payments?${params}`, {
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
      "data": {
        "list": [
          {
            "address": "string",
            "amount": 1,
            "currency": "string",
            "date": 1,
            "description": "string",
            "email": "ava@example.com",
            "expiredAt": 1,
            "network": "string",
            "orderId": "string",
            "payAmount": 1,
            "payCurrency": "string",
            "status": "string",
            "trackId": 1,
            "type": "string"
          }
        ],
        "meta": {
          "lastPage": 1,
          "page": 1,
          "total": 1
        }
      },
      "error": {},
      "message": "string",
      "status": 1,
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Payments action reference](actions/list-payments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oxaPayCryptoPaymentGateway/latest/actions/list-payments).

## Generate Invoice

Creates a new invoice in OxaPay.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/generate-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "currency": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/generate-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "currency": "string"
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
      "data": {
        "date": 1,
        "expiredAt": 1,
        "paymentUrl": "https://example.com",
        "trackId": 1
      },
      "error": {},
      "message": "string",
      "status": 1,
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Generate Invoice action reference](actions/generate-invoice.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oxaPayCryptoPaymentGateway/latest/actions/generate-invoice).
