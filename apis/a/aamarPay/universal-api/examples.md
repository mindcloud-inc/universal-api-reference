# aamarPay Universal API Examples

These examples use the MindCloud API key and aamarPay connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Transaction

Retrieves transaction details from aamarPay by merchant transaction ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aamarPay/latest/actions/search-transaction?connectionId=$CONNECTION_ID&requestId=1231231773" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestId": "1231231773"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/aamarPay/latest/actions/search-transaction?${params}`, {
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
      "amount": "string",
      "amountBdt": "string",
      "amountCurrency": "string",
      "amountOriginal": "string",
      "approvalCode": "string",
      "bankTrxid": "string",
      "binCardcategory": "string",
      "binCardtype": "string",
      "binCountry": "string",
      "binIssuer": "string",
      "callType": "string",
      "cardnumber": "string",
      "checkoutStatus": "string",
      "convertionRate": "string",
      "currency": "string",
      "currencyMerchant": "string",
      "cusAdd1": "string",
      "cusAdd2": "string",
      "cusCity": "string",
      "cusCountry": "string",
      "cusEmail": "ava@example.com",
      "cusFax": {},
      "cusName": "Ava Chen",
      "cusPhone": "string",
      "cusPostcode": {},
      "cusState": {},
      "date": "2026-05-07T12:00:00.000Z",
      "dateProcessed": "2026-05-07T12:00:00.000Z",
      "desc": "string",
      "docRecived": "string",
      "emailSend": "ava@example.com",
      "errorCode": "string",
      "errorTitle": "string",
      "ip": "string",
      "merchantId": "string",
      "merTxnid": "string",
      "optA": "string",
      "optB": "string",
      "optC": "string",
      "optD": "string",
      "paymentProcessor": "string",
      "paymentType": "string",
      "payStatus": "string",
      "pgTxnid": "string",
      "processingCharge": "string",
      "processingRatio": "string",
      "recAmount": "string",
      "riskLevel": "string",
      "riskTitle": "string",
      "shipAdd1": {},
      "shipAdd2": {},
      "shipCity": {},
      "shipCountry": {},
      "shipName": {},
      "shipPostcode": {},
      "shipState": {},
      "statusCode": "string",
      "statusTitle": "string",
      "storeAmount": "string",
      "storeId": "string",
      "verifyStatus": "string"
    }
  ],
  "meta": {}
}
```

See the full [Search Transaction action reference](actions/search-transaction.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aamarPay/latest/actions/search-transaction).

## Initiate Payment (Form Data)

Creates a payment request in aamarPay using form data.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aamarPay/latest/actions/initiate-payment-form-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "transactionId": "codex-form-20260407-1",
  "successUrl": "https://example.com/success",
  "failUrl": "https://example.com/fail",
  "cancelUrl": "https://example.com/cancel",
  "amount": "10.0",
  "currency": "BDT",
  "description": "Test transaction",
  "customerName": "Codex Test",
  "customerEmail": "test@example.com",
  "customerAddress1": "House 1",
  "customerCity": "Dhaka",
  "customerCountry": "Bangladesh",
  "customerPhone": "+8801704"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aamarPay/latest/actions/initiate-payment-form-data', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "transactionId": "codex-form-20260407-1",
    "successUrl": "https://example.com/success",
    "failUrl": "https://example.com/fail",
    "cancelUrl": "https://example.com/cancel",
    "amount": "10.0",
    "currency": "BDT",
    "description": "Test transaction",
    "customerName": "Codex Test",
    "customerEmail": "test@example.com",
    "customerAddress1": "House 1",
    "customerCity": "Dhaka",
    "customerCountry": "Bangladesh",
    "customerPhone": "+8801704"
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
      "paymentUrl": "https://example.com",
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Initiate Payment (Form Data) action reference](actions/initiate-payment-form-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aamarPay/latest/actions/initiate-payment-form-data).
