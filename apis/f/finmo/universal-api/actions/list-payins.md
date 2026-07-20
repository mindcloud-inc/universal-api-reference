# Finmo: List Payins

Retrieves payins from the Finmo platform.

```
GET https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-payins
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-payins?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-payins?${params}`, {
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
| `status` | string | no |  |
| `createdAt` | string | no |  |
| `customerId` | string | no |  |
| `creditWalletId` | string | no |  |
| `payinMethodName` | string | no |  |
| `startTime` | number | no |  |
| `endTime` | number | no |  |
| `limit` | number | no |  |
| `page` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        [
          {}
        ]
      ],
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
| `data[]` | array<object> |  |
| `data[].accountReceivableId` | object |  |
| `data[].additionalData` | object |  |
| `data[].additionalData.bankReferenceId` | object |  |
| `data[].advancedRedirectUrl` | object |  |
| `data[].amount` | number |  |
| `data[].cancelledAt` | object |  |
| `data[].checkoutId` | object |  |
| `data[].createdAt` | string |  |
| `data[].creditWalletId` | string |  |
| `data[].creditWalletTransactionId` | string |  |
| `data[].currency` | string |  |
| `data[].customerId` | object |  |
| `data[].description` | string |  |
| `data[].expireAt` | string |  |
| `data[].expiredAt` | object |  |
| `data[].feesCurrency` | string |  |
| `data[].feesIncludingTax` | number |  |
| `data[].feesWalletId` | string |  |
| `data[].feesWalletTransactionId` | string |  |
| `data[].feesWithoutTax` | number |  |
| `data[].isCancellable` | boolean |  |
| `data[].isChargeable` | boolean |  |
| `data[].isCompletelyRefunded` | boolean |  |
| `data[].isFeesCharged` | boolean |  |
| `data[].isMultipleRefundAllowed` | boolean |  |
| `data[].isOverRefundable` | boolean |  |
| `data[].isPaid` | boolean |  |
| `data[].isPartiallyPaid` | boolean |  |
| `data[].isPartiallyRefundable` | boolean |  |
| `data[].isReconciled` | boolean |  |
| `data[].isRefundable` | boolean |  |
| `data[].isRefundInitiated` | boolean |  |
| `data[].isSenderValidationEnabled` | boolean |  |
| `data[].metadata` | object |  |
| `data[].metadata.source` | string |  |
| `data[].metadata.testRun` | string |  |
| `data[].organizationReferenceId` | string |  |
| `data[].orgId` | string |  |
| `data[].paidAmount` | number |  |
| `data[].paidAt` | string |  |
| `data[].paidCurrency` | string |  |
| `data[].payCode` | object |  |
| `data[].payCode.text` | string |  |
| `data[].payinId` | string |  |
| `data[].payinMethodCategory` | string |  |
| `data[].payinMethodDescription` | string |  |
| `data[].payinMethodName` | string |  |
| `data[].payinMethodParam` | object |  |
| `data[].payinMethodParam.payidReference` | string |  |
| `data[].payinSenderIdList` | object |  |
| `data[].payinType` | string |  |
| `data[].pricingEventData` | object |  |
| `data[].pricingEventData.pAYINCOMPLETED` | object |  |
| `data[].pricingEventData.pAYINCOMPLETED.feesCurrency` | string |  |
| `data[].pricingEventData.pAYINCOMPLETED.feesIncludingTax` | number |  |
| `data[].pricingEventData.pAYINCOMPLETED.feesWithoutTax` | number |  |
| `data[].pricingEventData.pAYINCOMPLETED.taxOnFees` | number |  |
| `data[].pricingEventData.total` | object |  |
| `data[].pricingEventData.total.aggregatedFeesCurrency` | string |  |
| `data[].pricingEventData.total.aggregatedFeesIncludingTax` | number |  |
| `data[].pricingEventData.total.aggregatedFeesWithoutTax` | number |  |
| `data[].pricingEventData.total.aggregatedTaxOnFees` | number |  |
| `data[].receiptEmail` | object |  |
| `data[].redirectUrl` | object |  |
| `data[].refundAmountCompleted` | object |  |
| `data[].refundAmountRequested` | object |  |
| `data[].refundCurrencyCompleted` | object |  |
| `data[].refundCurrencyRequested` | object |  |
| `data[].refundStatus` | object |  |
| `data[].senderPartyDetail` | object |  |
| `data[].senderPartyDetail.accountHolderName` | string |  |
| `data[].senderPartyDetail.accountNumber` | string |  |
| `data[].senderPartyDetail.bsb` | string |  |
| `data[].senderPartyDetail.payId` | string |  |
| `data[].senderPartyDetail.payIdType` | string |  |
| `data[].status` | string |  |
| `data[].taxOnFees` | object |  |
| `data[].transactionId` | string |  |
| `data[].updatedAt` | string |  |
| `data[].virtualAccountId` | object |  |
| `data[].webhookUrl` | object |  |
| `requestId` | string |  |
| `requestTime` | string |  |
| `statusCode` | number |  |
| `statusText` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Finmo API, this operation is `GET /payin` (base URL `https://api.finmo.net/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payins.md) for the provider-specific parameters and requirements.

