# Zoho Books: Retrieve Customer Payment



```
GET https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/retrieve-customer-payment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/retrieve-customer-payment?connectionId=$CONNECTION_ID&organizationId=string&payment_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string",
  "payment_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/retrieve-customer-payment?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accept` | string | no | Response format: json or pdf. |
| `organizationId` | string | yes | ID of the organization. |
| `payment_id` | string | yes | Unique identifier of the payment. |

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

Through the native Zoho Books API, this operation is `GET /customerpayments/:payment_id` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-customer-payment.md) for the provider-specific parameters and requirements.

