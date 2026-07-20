# Finmo: Retrieve Payin

Finds a payin in Finmo by ID.

```
GET https://connect.mindcloud.co/v1/universal/finmo/latest/actions/retrieve-payin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/retrieve-payin?connectionId=$CONNECTION_ID&payinId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "payinId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finmo/latest/actions/retrieve-payin?${params}`, {
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
| `payinId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "accountReceivableId": {},
        "additionalData": {},
        "advancedRedirectUrl": {},
        "amount": 1,
        "cancelledAt": {},
        "checkoutId": {},
        "createdAt": "string",
        "creditWalletId": "string",
        "creditWalletTransactionId": {},
        "currency": "string",
        "customerId": {},
        "description": "string",
        "expireAt": "string",
        "expiredAt": {},
        "feesCurrency": {},
        "feesIncludingTax": {},
        "feesWalletId": "string",
        "feesWalletTransactionId": {},
        "feesWithoutTax": {},
        "isCancellable": true,
        "isChargeable": true,
        "isCompletelyRefunded": true,
        "isFeesCharged": true,
        "isMultipleRefundAllowed": true,
        "isOverRefundable": true,
        "isPaid": true,
        "isPartiallyPaid": true,
        "isPartiallyRefundable": true,
        "isReconciled": true,
        "isRefundable": true,
        "isRefundInitiated": true,
        "isSenderValidationEnabled": true,
        "metadata": {
          "source": "string",
          "testRun": "string"
        },
        "organizationReferenceId": "string",
        "orgId": "string",
        "paidAmount": {},
        "paidAt": {},
        "paidCurrency": {},
        "payCode": {
          "text": "string"
        },
        "payinId": "string",
        "payinMethodCategory": "string",
        "payinMethodDescription": "string",
        "payinMethodName": "Ava Chen",
        "payinMethodParam": {
          "payidReference": "string"
        },
        "payinSenderIdList": {},
        "payinType": "string",
        "pricingEventData": {},
        "receiptEmail": {},
        "redirectUrl": {},
        "refundAmountCompleted": {},
        "refundAmountRequested": {},
        "refundCurrencyCompleted": {},
        "refundCurrencyRequested": {},
        "refundStatus": {},
        "senderPartyDetail": {},
        "status": "string",
        "taxOnFees": {},
        "transactionId": {},
        "updatedAt": "string",
        "virtualAccountId": {},
        "webhookUrl": {}
      },
      "requestId": "string",
      "requestTime": "string",
      "statusCode": 1,
      "statusText": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.accountReceivableId` | object |  |
| `data.additionalData` | object |  |
| `data.advancedRedirectUrl` | object |  |
| `data.amount` | number |  |
| `data.cancelledAt` | object |  |
| `data.checkoutId` | object |  |
| `data.createdAt` | string |  |
| `data.creditWalletId` | string |  |
| `data.creditWalletTransactionId` | object |  |
| `data.currency` | string |  |
| `data.customerId` | object |  |
| `data.description` | string |  |
| `data.expireAt` | string |  |
| `data.expiredAt` | object |  |
| `data.feesCurrency` | object |  |
| `data.feesIncludingTax` | object |  |
| `data.feesWalletId` | string |  |
| `data.feesWalletTransactionId` | object |  |
| `data.feesWithoutTax` | object |  |
| `data.isCancellable` | boolean |  |
| `data.isChargeable` | boolean |  |
| `data.isCompletelyRefunded` | boolean |  |
| `data.isFeesCharged` | boolean |  |
| `data.isMultipleRefundAllowed` | boolean |  |
| `data.isOverRefundable` | boolean |  |
| `data.isPaid` | boolean |  |
| `data.isPartiallyPaid` | boolean |  |
| `data.isPartiallyRefundable` | boolean |  |
| `data.isReconciled` | boolean |  |
| `data.isRefundable` | boolean |  |
| `data.isRefundInitiated` | boolean |  |
| `data.isSenderValidationEnabled` | boolean |  |
| `data.metadata` | object |  |
| `data.metadata.source` | string |  |
| `data.metadata.testRun` | string |  |
| `data.organizationReferenceId` | string |  |
| `data.orgId` | string |  |
| `data.paidAmount` | object |  |
| `data.paidAt` | object |  |
| `data.paidCurrency` | object |  |
| `data.payCode` | object |  |
| `data.payCode.text` | string |  |
| `data.payinId` | string |  |
| `data.payinMethodCategory` | string |  |
| `data.payinMethodDescription` | string |  |
| `data.payinMethodName` | string |  |
| `data.payinMethodParam` | object |  |
| `data.payinMethodParam.payidReference` | string |  |
| `data.payinSenderIdList` | object |  |
| `data.payinType` | string |  |
| `data.pricingEventData` | object |  |
| `data.receiptEmail` | object |  |
| `data.redirectUrl` | object |  |
| `data.refundAmountCompleted` | object |  |
| `data.refundAmountRequested` | object |  |
| `data.refundCurrencyCompleted` | object |  |
| `data.refundCurrencyRequested` | object |  |
| `data.refundStatus` | object |  |
| `data.senderPartyDetail` | object |  |
| `data.status` | string |  |
| `data.taxOnFees` | object |  |
| `data.transactionId` | object |  |
| `data.updatedAt` | string |  |
| `data.virtualAccountId` | object |  |
| `data.webhookUrl` | object |  |
| `requestId` | string |  |
| `requestTime` | string |  |
| `statusCode` | number |  |
| `statusText` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Finmo API, this operation is `GET /payin/:payin_id` (base URL `https://api.finmo.net/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-payin.md) for the provider-specific parameters and requirements.

