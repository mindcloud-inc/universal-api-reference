# Moxie: Apply Payment to Invoice

Applies a payment to an invoice in Moxie.

```
POST https://connect.mindcloud.co/v1/universal/moxie/latest/actions/apply-payment-to-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moxie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moxie/latest/actions/apply-payment-to-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "date": "2026-03-15",
  "amount": 1,
  "invoiceNumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moxie/latest/actions/apply-payment-to-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "date": "2026-03-15",
    "amount": 1,
    "invoiceNumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date` | string | yes | Payment date in YYYY-MM-DD format. Example: `2026-03-15`. |
| `amount` | number | yes | Payment amount. |
| `invoiceNumber` | string | yes | Invoice number to apply the payment to. |
| `clientName` | string | no | Client name tied to the invoice. |
| `paymentType` | string | no | Optional payment type enum. Use one of OTHER, VENMO, PAYPAL, APP_PAYOUT, CREDIT_CARD, CHECK, ZELLE, STRIPE, BANK_TRANSFER, or CASH. Example: `CREDIT_CARD`. |
| `referenceNumber` | string | no | Reference number for the payment. |
| `memo` | string | no | Internal payment memo. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "amountDue": 1,
      "clientId": "string",
      "clientInfo": {},
      "currency": "string",
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "datePaid": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "invoiceNumber": 1,
      "invoiceNumberFormatted": "string",
      "payments": [
        {}
      ],
      "paymentTotal": 1,
      "status": "string",
      "total": 1,
      "viewOnlineUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number |  |
| `amountDue` | number |  |
| `clientId` | string |  |
| `clientInfo` | object |  |
| `currency` | string |  |
| `dateCreated` | date |  |
| `datePaid` | date |  |
| `id` | string |  |
| `invoiceNumber` | number |  |
| `invoiceNumberFormatted` | string |  |
| `payments` | array<object> |  |
| `paymentTotal` | number |  |
| `status` | string |  |
| `total` | number |  |
| `viewOnlineUrl` | string |  |

## Native endpoint

Through the native Moxie API, this operation is `POST /action/payment/create` (base URL `https://pod01.withmoxie.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/apply-payment-to-invoice.md) for the provider-specific parameters and requirements.

