# Zoho Invoice: Create Payment

Creates a payment in Zoho Invoice.

```
POST https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/create-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Invoice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/create-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string",
  "customerId": "string",
  "paymentMode": "string",
  "amount": 1,
  "date": "2026-05-07T12:00:00.000Z",
  "invoices[]": [
    {}
  ],
  "invoices[].invoiceId": "string",
  "invoices[].amountApplied": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoInvoice/latest/actions/create-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string",
    "customerId": "string",
    "paymentMode": "string",
    "amount": 1,
    "date": "2026-05-07T12:00:00.000Z",
    "invoices[]": [{}],
    "invoices[].invoiceId": "string",
    "invoices[].amountApplied": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | list<string> | yes | Unique identifier of the organization. |
| `customerId` | string | yes | Customer ID of the customer for whom the payment is recorded. |
| `paymentMode` | string | yes | Mode of payment. |
| `amount` | number | yes | Amount received in the payment. |
| `date` | date | yes | Date on which the payment is made. |
| `referenceNumber` | string | no | Reference number for the payment. |
| `description` | string | no | Description of the payment. |
| `invoices[]` | array<object> | yes | Invoices associated with the payment. |
| `invoices[].invoiceId` | string | yes | Invoice ID of the required invoice. |
| `invoices[].amountApplied` | number | yes | Amount paid for the invoice. |
| `exchangeRate` | number | no | Exchange rate for the currency used in the invoices and the customer's currency. |
| `customFields[]` | array<object> | no | Custom fields for the payment. |
| `customFields[].label` | string | no | Name of the custom field. |
| `customFields[].value` | string | no | Value of the custom field. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `paymentForm` | string | no | Mode of vendor payment. |
| `bankCharges` | number | no | Additional bank charges. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "createdTime": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "customerId": "string",
      "customerName": "Ava Chen",
      "date": "2026-05-07T12:00:00.000Z",
      "paymentId": "string",
      "paymentMode": "string",
      "paymentNumber": "string",
      "paymentStatus": "string",
      "referenceNumber": "string",
      "unusedAmount": 1,
      "updatedTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `createdTime` | date |  |
| `currencyCode` | string |  |
| `customerId` | string |  |
| `customerName` | string |  |
| `date` | date |  |
| `paymentId` | string |  |
| `paymentMode` | string |  |
| `paymentNumber` | string |  |
| `paymentStatus` | string |  |
| `referenceNumber` | string |  |
| `unusedAmount` | number |  |
| `updatedTime` | date |  |

## Native endpoint

Through the native Zoho Invoice API, this operation is `POST /customerpayments` (base URL `https://www.zohoapis.com/invoice/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment.md) for the provider-specific parameters and requirements.

