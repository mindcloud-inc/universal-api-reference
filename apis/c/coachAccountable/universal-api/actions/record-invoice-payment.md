# CoachAccountable: Record Invoice Payment

Records an invoice payment in CoachAccountable.

```
POST https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/record-invoice-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoachAccountable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/record-invoice-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoiceId": 1,
  "amount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coachAccountable/latest/actions/record-invoice-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoiceId": 1,
    "amount": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceId` | number | yes | The ID of the Invoice to which the record of payment is to be added. Invoice Number also accepted when prefixed with a "#", e.g. "#1005". |
| `dateOf` | date | no | Will fill in as the current time when not supplied. Future dates not allowed. |
| `amount` | number | yes |  |
| `method` | list | no | If not supplied, will assume "Credit Card" One of: `Bank Transfer`, `Cash`, `Check`, `Credit Card`, `Other`. Default: `Credit Card`. |
| `checkNumber` | string | no | Optional memo that will be saved when supplied and method="Check" |
| `allowOverpay` | boolean | no | If not set to "true", will throw an error if the added payment results in a net overpay of the invoice. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "PaymentID": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `PaymentID` | number |  |

## Native endpoint

Through the native CoachAccountable API, this operation is `POST /` (base URL `https://www.coachaccountable.com/API`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/record-invoice-payment.md) for the provider-specific parameters and requirements.

