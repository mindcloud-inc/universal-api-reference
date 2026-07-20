# Finmo: List Virtual Accounts

Retrieves virtual accounts from the Finmo platform.

```
GET https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-virtual-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finmo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-virtual-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finmo/latest/actions/list-virtual-accounts?${params}`, {
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
| `customerId` | string | no | Filter virtual accounts for a specific customer. |
| `includeDeleted` | boolean | no | Include deleted virtual accounts. |
| `createdAt` | string | no | Filter by UTC creation date (YYYY-MM-DD). |
| `startTime` | number | no | Filter from epoch start timestamp. |
| `endTime` | number | no | Filter to epoch end timestamp. |
| `limit` | number | no | Maximum number of records per page. |
| `page` | number | no | Page number to return. |

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
| `data[].category` | string |  |
| `data[].createdAt` | string |  |
| `data[].creditWalletId` | string |  |
| `data[].currency` | string |  |
| `data[].customerId` | string |  |
| `data[].deletedAt` | string |  |
| `data[].description` | string |  |
| `data[].expireAt` | object |  |
| `data[].expiredAt` | object |  |
| `data[].feesCurrency` | string |  |
| `data[].feesIncludingTax` | number |  |
| `data[].feesWithoutTax` | number |  |
| `data[].isActive` | boolean |  |
| `data[].isCancellable` | boolean |  |
| `data[].isChargeable` | boolean |  |
| `data[].isDeleted` | boolean |  |
| `data[].isExpired` | boolean |  |
| `data[].isFeesCharged` | boolean |  |
| `data[].isRefundable` | boolean |  |
| `data[].isSenderValidationEnabled` | boolean |  |
| `data[].metadata` | object |  |
| `data[].metadata.source` | string |  |
| `data[].metadata.testRun` | string |  |
| `data[].organizationReferenceId` | object |  |
| `data[].orgId` | string |  |
| `data[].payCode` | object |  |
| `data[].payCode.accountName` | string |  |
| `data[].payCode.accountNumber` | string |  |
| `data[].payCode.bankAddress` | string |  |
| `data[].payCode.bankCountry` | string |  |
| `data[].payCode.bankName` | string |  |
| `data[].payCode.bicSwift` | string |  |
| `data[].payCode.currency` | string |  |
| `data[].payinMethodName` | string |  |
| `data[].payinMethodParam` | object |  |
| `data[].payinSenderIdList` | object |  |
| `data[].scope` | string |  |
| `data[].taxOnFees` | object |  |
| `data[].transactionId` | string |  |
| `data[].updatedAt` | string |  |
| `data[].virtualAccountId` | string |  |
| `data[].webhookUrl` | object |  |
| `requestId` | string |  |
| `requestTime` | string |  |
| `statusCode` | number |  |
| `statusText` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Finmo API, this operation is `GET /virtual-account` (base URL `https://api.finmo.net/v1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-virtual-accounts.md) for the provider-specific parameters and requirements.

