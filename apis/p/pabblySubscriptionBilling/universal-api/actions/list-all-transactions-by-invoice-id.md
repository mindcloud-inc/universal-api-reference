# Pabbly Subscription Billing: List All Transactions By Invoice Id



```
GET https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-transactions-by-invoice-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-transactions-by-invoice-id?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/list-all-transactions-by-invoice-id?${params}`, {
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
      "message": [
        {
          "planId": "string",
          "productId": "string",
          "referenceId": "string",
          "statusFormatted": "string",
          "subscriptionId": "string",
          "transaction": {
            "amount": 1,
            "amountCapturable": 1,
            "amountDetails": {
              "tip": {
                "amount": 1
              }
            },
            "amountReceived": 1,
            "application": "string",
            "applicationFeeAmount": 1,
            "automaticPaymentMethods": "string",
            "canceledAt": "2026-05-07T12:00:00.000Z",
            "cancellationReason": "string",
            "captureMethod": "string",
            "charges": {
              "data": [
                {
                  "amount": 1,
                  "amountCaptured": 1,
                  "amountRefunded": 1,
                  "id": "string",
                  "object": "string"
                }
              ],
              "object": "string"
            },
            "id": "string",
            "object": "string"
          },
          "typeFormated": "string"
        }
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message[].planId` | string |  |
| `message[].productId` | string |  |
| `message[].referenceId` | string |  |
| `message[].statusFormatted` | string |  |
| `message[].subscriptionId` | string |  |
| `message[].transaction.amount` | number |  |
| `message[].transaction.amountCapturable` | number |  |
| `message[].transaction.amountDetails.tip.amount` | number |  |
| `message[].transaction.amountReceived` | number |  |
| `message[].transaction.application` | string |  |
| `message[].transaction.applicationFeeAmount` | number |  |
| `message[].transaction.automaticPaymentMethods` | string |  |
| `message[].transaction.canceledAt` | date |  |
| `message[].transaction.cancellationReason` | string |  |
| `message[].transaction.captureMethod` | string |  |
| `message[].transaction.charges.data[].amount` | number |  |
| `message[].transaction.charges.data[].amountCaptured` | number |  |
| `message[].transaction.charges.data[].amountRefunded` | number |  |
| `message[].transaction.charges.data[].id` | string |  |
| `message[].transaction.charges.data[].object` | string |  |
| `message[].transaction.charges.object` | string |  |
| `message[].transaction.id` | string |  |
| `message[].transaction.object` | string |  |
| `message[].typeFormated` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `GET /v1/invoices/transactions/:invoiceId` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-transactions-by-invoice-id.md) for the provider-specific parameters and requirements.

