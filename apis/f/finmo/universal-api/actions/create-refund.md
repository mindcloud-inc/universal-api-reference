# Finmo: Create Refund

Creates a new refund in Finmo.

```
POST https://connect.mindcloud.co/v1/universal/finmo/latest/actions/create-refund
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/create-refund" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "payinId": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/finmo/latest/actions/create-refund', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "payinId": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `payinId` | string | yes |  |
| `type` | string | yes |  |
| `amount` | number | no |  |
| `currency` | string | no |  |
| `organizationReferenceId` | string | no |  |
| `webhookUrl` | string | no |  |
| `metadata` | object | no |  |

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

Through the native Finmo API, this operation is `POST /refund` (base URL `https://api.finmo.net/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-refund.md) for the provider-specific parameters and requirements.

