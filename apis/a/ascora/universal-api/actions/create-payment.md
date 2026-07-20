# Ascora: Create Payment

Creates a new payment in Ascora.

```
POST https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceNumber": "string",
  "paymentAmount": 1,
  "paymentDate": "2026-05-07T12:00:00.000Z",
  "paymentMethod": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceNumber": "string",
    "paymentAmount": 1,
    "paymentDate": "2026-05-07T12:00:00.000Z",
    "paymentMethod": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `comment` | string | no | Free text comment associated with the Payment. |
| `invoiceNumber` | string | yes | Invoice Number in Ascora to which the Payment will be applied. |
| `paymentAmount` | number | yes | Amount of the Payment not including any credit card surcharge. |
| `paymentDate` | date | yes | Date associated with the Payment. |
| `paymentMethod` | string | yes | Name of the related Payment Method in Ascora. |
| `receiptNumber` | string | no | Transaction receipt number associated with the Payment. |
| `surchargeAmount` | number | no | Amount of any surcharge associated with processing the payment. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ascora API returns.

## Native endpoint

Through the native Ascora API, this operation is `POST /Accounting/CreatePayment` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment.md) for the provider-specific parameters and requirements.

