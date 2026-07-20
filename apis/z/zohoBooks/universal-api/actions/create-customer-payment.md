# Zoho Books: Create Customer Payment



```
POST https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/create-customer-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/create-customer-payment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "customerId": "string",
  "date": "string",
  "invoiceId": "string",
  "invoices[]": [
    {}
  ],
  "organizationId": "string",
  "paymentMode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/create-customer-payment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "customerId": "string",
    "date": "string",
    "invoiceId": "string",
    "invoices[]": [{}],
    "organizationId": "string",
    "paymentMode": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | Payment amount. |
| `amountApplied` | number | no | Top-level applied amount documented by Zoho for payment creation. |
| `customerId` | string | yes | Customer involved in the payment. |
| `date` | string | yes | Payment date. |
| `description` | string | no | Payment description. |
| `invoiceId` | string | yes | Top-level invoice identifier documented by Zoho for payment creation. |
| `invoices[]` | array<object> | yes | Invoices associated with the payment. |
| `invoices[].amountApplied` | number | no | Amount applied to the invoice inside the invoices array. |
| `invoices[].invoiceId` | string | no | Invoice identifier inside the invoices array. |
| `organizationId` | string | yes | ID of the organization. |
| `paymentMode` | string | yes | Payment mode. |
| `referenceNumber` | string | no | Reference number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string",
      "payment": {
        "accountId": "string",
        "accountName": "Ava Chen",
        "accountType": "string",
        "amount": 1,
        "bankCharges": 1,
        "canSendInMail": true,
        "canSendPaymentSms": true,
        "createdBy": "string",
        "createdTime": "2026-05-07T12:00:00.000Z",
        "currencyCode": "string",
        "currencyId": "string",
        "currencySymbol": "string",
        "customerAdvanceAccountId": "string",
        "customerAdvanceAccountName": "Ava Chen",
        "customerId": "string",
        "customerName": "Ava Chen",
        "date": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "discountAmount": 1,
        "exchangeRate": 1,
        "invoices": [
          {}
        ],
        "isPaymentDetailsRequired": true,
        "lastFourDigits": "string",
        "lockDetails": {
          "canLock": true
        },
        "paymentGateway": "string",
        "paymentId": "string",
        "paymentLinkId": "https://example.com",
        "paymentMode": "string",
        "paymentNumber": "string",
        "paymentStatus": "string",
        "pricePrecision": 1,
        "referenceNumber": "string",
        "roundingMode": "string",
        "settlementStatus": "string",
        "taxAmountWithheld": 1,
        "templateId": "string",
        "templateName": "Ava Chen",
        "unusedAmount": 1,
        "updatedTime": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `message` | string |  |
| `payment.accountId` | string |  |
| `payment.accountName` | string |  |
| `payment.accountType` | string |  |
| `payment.amount` | number |  |
| `payment.bankCharges` | number |  |
| `payment.canSendInMail` | boolean |  |
| `payment.canSendPaymentSms` | boolean |  |
| `payment.createdBy` | string |  |
| `payment.createdTime` | date |  |
| `payment.currencyCode` | string |  |
| `payment.currencyId` | string |  |
| `payment.currencySymbol` | string |  |
| `payment.customerAdvanceAccountId` | string |  |
| `payment.customerAdvanceAccountName` | string |  |
| `payment.customerId` | string |  |
| `payment.customerName` | string |  |
| `payment.date` | date |  |
| `payment.description` | string |  |
| `payment.discountAmount` | number |  |
| `payment.exchangeRate` | number |  |
| `payment.invoices` | array<object> |  |
| `payment.isPaymentDetailsRequired` | boolean |  |
| `payment.lastFourDigits` | string |  |
| `payment.lockDetails.canLock` | boolean |  |
| `payment.paymentGateway` | string |  |
| `payment.paymentId` | string |  |
| `payment.paymentLinkId` | string |  |
| `payment.paymentMode` | string |  |
| `payment.paymentNumber` | string |  |
| `payment.paymentStatus` | string |  |
| `payment.pricePrecision` | number |  |
| `payment.referenceNumber` | string |  |
| `payment.roundingMode` | string |  |
| `payment.settlementStatus` | string |  |
| `payment.taxAmountWithheld` | number |  |
| `payment.templateId` | string |  |
| `payment.templateName` | string |  |
| `payment.unusedAmount` | number |  |
| `payment.updatedTime` | date |  |

## Native endpoint

Through the native Zoho Books API, this operation is `POST /customerpayments` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-payment.md) for the provider-specific parameters and requirements.

