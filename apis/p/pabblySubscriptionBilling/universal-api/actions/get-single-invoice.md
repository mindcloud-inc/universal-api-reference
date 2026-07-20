# Pabbly Subscription Billing: Get Single Invoice



```
GET https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-single-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-single-invoice?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/get-single-invoice?${params}`, {
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
| `invoiceId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creditNote": {
        "chargeAmount": 1,
        "creditApplied": [
          "string"
        ],
        "newPlanTotal": 1,
        "status": "string",
        "totalCreditAmount": 1,
        "totalTax": "string"
      },
      "cronProcess": "string",
      "currencySymbol": "string",
      "customerId": "string",
      "id": "string",
      "invoiceId": "string",
      "productId": "string",
      "quantity": 1,
      "retry": true,
      "retryCount": 1,
      "setupFee": 1,
      "status": "string",
      "subscriptionId": "string",
      "taxApply": {
        "country": "string",
        "exemptTax": [
          "string"
        ],
        "taxId": "string",
        "totalAmount": 1,
        "totalTax": "string"
      },
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `creditNote.chargeAmount` | number |  |
| `creditNote.creditApplied[]` | string |  |
| `creditNote.newPlanTotal` | number |  |
| `creditNote.status` | string |  |
| `creditNote.totalCreditAmount` | number |  |
| `creditNote.totalTax` | string |  |
| `cronProcess` | string |  |
| `currencySymbol` | string |  |
| `customerId` | string |  |
| `id` | string |  |
| `invoiceId` | string |  |
| `productId` | string |  |
| `quantity` | number |  |
| `retry` | boolean |  |
| `retryCount` | number |  |
| `setupFee` | number |  |
| `status` | string |  |
| `subscriptionId` | string |  |
| `taxApply.country` | string |  |
| `taxApply.exemptTax[]` | string |  |
| `taxApply.taxId` | string |  |
| `taxApply.totalAmount` | number |  |
| `taxApply.totalTax` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `GET /v1/invoice/:invoiceId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-single-invoice.md) for the provider-specific parameters and requirements.

