# Bexio: Create Invoice Payment

Creates an invoice payment in Bexio.

```
POST https://connect.mindcloud.co/v1/universal/bexio/latest/actions/create-invoice-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bexio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bexio/latest/actions/create-invoice-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceId": 1,
  "value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bexio/latest/actions/create-invoice-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceId": 1,
    "value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceId` | number | yes | The ID of the invoice. |
| `date` | date | no | The payment date. |
| `value` | string | yes | The payment value. |
| `bankAccountId` | number | no | References a bank account object. |
| `paymentServiceId` | number | no | References a payment service. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bankAccountId": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "isCashDiscount": true,
      "isClientAccountRedemption": true,
      "kbBillId": {},
      "kbCreditVoucherId": {},
      "kbCreditVoucherText": "string",
      "kbInvoiceId": 1,
      "paymentServiceId": {},
      "title": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bankAccountId` | number |  |
| `date` | date |  |
| `id` | number |  |
| `isCashDiscount` | boolean |  |
| `isClientAccountRedemption` | boolean |  |
| `kbBillId` | object |  |
| `kbCreditVoucherId` | object |  |
| `kbCreditVoucherText` | string |  |
| `kbInvoiceId` | number |  |
| `paymentServiceId` | object |  |
| `title` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Bexio API, this operation is `POST /2.0/kb_invoice/:invoice_id/payment` (base URL `https://api.bexio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invoice-payment.md) for the provider-specific parameters and requirements.

