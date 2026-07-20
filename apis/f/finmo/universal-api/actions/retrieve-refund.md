# Finmo: Retrieve Refund

Finds a refund in Finmo by ID.

```
GET https://connect.mindcloud.co/v1/universal/finmo/latest/actions/retrieve-refund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/retrieve-refund?connectionId=$CONNECTION_ID&refundId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "refundId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finmo/latest/actions/retrieve-refund?${params}`, {
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
| `refundId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "amount": 1,
        "createdAt": "string",
        "currency": "string",
        "customerId": {},
        "debitWalletId": "string",
        "debitWalletTransactionId": "string",
        "description": {},
        "feesCurrency": "string",
        "feesIncludingTax": 1,
        "feesWalletId": "string",
        "feesWalletTransactionId": "string",
        "feesWithoutTax": 1,
        "isFeesCharged": true,
        "metadata": {
          "source": "string",
          "testRun": "string"
        },
        "organizationReferenceId": "string",
        "orgId": "string",
        "payinId": "string",
        "payinMethodName": "Ava Chen",
        "reasonForFailure": {},
        "receiptEmail": {},
        "refundedAt": {},
        "refundId": "string",
        "status": "string",
        "taxOnFees": 1,
        "transactionId": {},
        "type": "string",
        "updatedAt": "string",
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
| `data.amount` | number |  |
| `data.createdAt` | string |  |
| `data.currency` | string |  |
| `data.customerId` | object |  |
| `data.debitWalletId` | string |  |
| `data.debitWalletTransactionId` | string |  |
| `data.description` | object |  |
| `data.feesCurrency` | string |  |
| `data.feesIncludingTax` | number |  |
| `data.feesWalletId` | string |  |
| `data.feesWalletTransactionId` | string |  |
| `data.feesWithoutTax` | number |  |
| `data.isFeesCharged` | boolean |  |
| `data.metadata` | object |  |
| `data.metadata.source` | string |  |
| `data.metadata.testRun` | string |  |
| `data.organizationReferenceId` | string |  |
| `data.orgId` | string |  |
| `data.payinId` | string |  |
| `data.payinMethodName` | string |  |
| `data.reasonForFailure` | object |  |
| `data.receiptEmail` | object |  |
| `data.refundedAt` | object |  |
| `data.refundId` | string |  |
| `data.status` | string |  |
| `data.taxOnFees` | number |  |
| `data.transactionId` | object |  |
| `data.type` | string |  |
| `data.updatedAt` | string |  |
| `data.webhookUrl` | object |  |
| `requestId` | string |  |
| `requestTime` | string |  |
| `statusCode` | number |  |
| `statusText` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Finmo API, this operation is `GET /refund/:refund_id` (base URL `https://api.finmo.net/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-refund.md) for the provider-specific parameters and requirements.

