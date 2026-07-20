# iPaymu: List Transaction History

List your iPaymu transaction history.

```
GET https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/list-transaction-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iPaymu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/list-transaction-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/list-transaction-history?${params}`, {
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
| `page` | number | no | Page number. Default: `1`. |
| `limit` | number | no | Number of records to return. Default: `20`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pagination": {
        "count": 1,
        "currentPage": 1,
        "perPage": 1,
        "total": 1,
        "totalPages": 1
      },
      "transaction": [
        {
          "amount": 1,
          "buyerEmail": "ava@example.com",
          "buyerName": "Ava Chen",
          "buyerPhone": "string",
          "createdDate": "string",
          "expiredDate": "string",
          "fee": 1,
          "isEscrow": true,
          "isLocked": true,
          "notes": "string",
          "paidStatus": "string",
          "paymentChannel": "string",
          "paymentCode": "string",
          "paymentMethod": "string",
          "paymentName": "Ava Chen",
          "receiver": "string",
          "referenceId": "string",
          "relatedId": 1,
          "sender": "string",
          "sessionId": "string",
          "settlementDate": {},
          "status": 1,
          "statusDesc": "string",
          "subTotal": 1,
          "successDate": {},
          "transactionId": 1,
          "type": 1,
          "typeDesc": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pagination.count` | number |  |
| `pagination.currentPage` | number |  |
| `pagination.perPage` | number |  |
| `pagination.total` | number |  |
| `pagination.totalPages` | number |  |
| `transaction[].amount` | number |  |
| `transaction[].buyerEmail` | string |  |
| `transaction[].buyerName` | string |  |
| `transaction[].buyerPhone` | string |  |
| `transaction[].createdDate` | string |  |
| `transaction[].expiredDate` | string |  |
| `transaction[].fee` | number |  |
| `transaction[].isEscrow` | boolean |  |
| `transaction[].isLocked` | boolean |  |
| `transaction[].notes` | string |  |
| `transaction[].paidStatus` | string |  |
| `transaction[].paymentChannel` | string |  |
| `transaction[].paymentCode` | string |  |
| `transaction[].paymentMethod` | string |  |
| `transaction[].paymentName` | string |  |
| `transaction[].receiver` | string |  |
| `transaction[].referenceId` | string |  |
| `transaction[].relatedId` | number |  |
| `transaction[].sender` | string |  |
| `transaction[].sessionId` | string |  |
| `transaction[].settlementDate` | object |  |
| `transaction[].status` | number |  |
| `transaction[].statusDesc` | string |  |
| `transaction[].subTotal` | number |  |
| `transaction[].successDate` | object |  |
| `transaction[].transactionId` | number |  |
| `transaction[].type` | number |  |
| `transaction[].typeDesc` | string |  |

## Native endpoint

Through the native iPaymu API, this operation is `POST /history` (base URL `https://my.ipaymu.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transaction-history.md) for the provider-specific parameters and requirements.

