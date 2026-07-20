# Avaza: Create Payment

Creates a new payment in Avaza.

```
POST https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Avaza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "paymentallocations": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avaza/latest/actions/create-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "paymentallocations": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | no |  |
| `paymentnumber` | string | no | Optional. If not specified will be automatically generated |
| `dateissued` | date | no | Date of Payment. If not specified, assumes today. |
| `transactionprefix` | string | no | Optional to override the default prefix added to Payment Numbers |
| `customeridfk` | number | no | Only required if no invoice allocations specified. |
| `exchangerate` | number | no | Optional. Only used when the Customer's currecy is different from the Avaza account's base currency. Specifies the exchange rate that should apply between the customer currency and base currency. If not provided we will obtain an up to date exchange rate for the Payment Issue Date. |
| `transactionreference` | string | no | Optional for storing the reference # of the payment method. |
| `notes` | string | no |  |
| `paymentprovidercode` | string | no | Optional for storing the payment provider who was the source of funds. |
| `paymentallocations` | list<object> | yes | List of amounts within this payment that are allocated to invoices. The sum of these be less than or equal to the payment amount. |
| `paymentallocations[].invoicetransactionidfk` | number | no | The Avaza Invoice TransactionID that is having a payment amount allocated to it. |
| `paymentallocations[].allocationamount` | number | no | The Amount being allocated to the invoice. Expects same currency as invoice currency |
| `paymentallocations[].allocationdate` | date | no | Optional. Defaults to the current time in the Avaza account's timezone. The date the allocation is applied to the invoice. Can be difference from the Payment Date when doing prepayments etc. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Avaza API returns.

## Native endpoint

Through the native Avaza API, this operation is `POST /api/Payment` (base URL `https://api.avaza.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment.md) for the provider-specific parameters and requirements.

