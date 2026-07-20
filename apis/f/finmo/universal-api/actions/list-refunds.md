# Finmo: List Refunds

Retrieves refunds from the Finmo platform.

```
GET https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-refunds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-refunds?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-refunds?${params}`, {
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
| `payinId` | string | no |  |
| `amount` | number | no |  |
| `createdAt` | string | no |  |
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
| `data[].amount` | number |  |
| `data[].createdAt` | string |  |
| `data[].currency` | string |  |
| `data[].customerId` | object |  |
| `data[].debitWalletId` | string |  |
| `data[].debitWalletTransactionId` | string |  |
| `data[].description` | object |  |
| `data[].feesCurrency` | string |  |
| `data[].feesIncludingTax` | number |  |
| `data[].feesWalletId` | string |  |
| `data[].feesWalletTransactionId` | string |  |
| `data[].feesWithoutTax` | number |  |
| `data[].isFeesCharged` | boolean |  |
| `data[].metadata` | object |  |
| `data[].metadata.source` | string |  |
| `data[].metadata.testRun` | string |  |
| `data[].organizationReferenceId` | string |  |
| `data[].orgId` | string |  |
| `data[].payinId` | string |  |
| `data[].payinMethodName` | string |  |
| `data[].reasonForFailure` | object |  |
| `data[].receiptEmail` | object |  |
| `data[].refundedAt` | object |  |
| `data[].refundId` | string |  |
| `data[].status` | string |  |
| `data[].taxOnFees` | number |  |
| `data[].transactionId` | object |  |
| `data[].type` | string |  |
| `data[].updatedAt` | string |  |
| `data[].webhookUrl` | object |  |
| `requestId` | string |  |
| `requestTime` | string |  |
| `statusCode` | number |  |
| `statusText` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Finmo API, this operation is `GET /refund` (base URL `https://api.finmo.net/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-refunds.md) for the provider-specific parameters and requirements.

