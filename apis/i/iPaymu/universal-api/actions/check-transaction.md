# iPaymu: Check Transaction

Get realtime details and status for an iPaymu transaction.

```
GET https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/check-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iPaymu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/check-transaction?connectionId=$CONNECTION_ID&transactionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/iPaymu/latest/actions/check-transaction?${params}`, {
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
| `transactionId` | number | yes | iPaymu transaction identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "buyerEmail": "ava@example.com",
      "buyerName": "Ava Chen",
      "buyerPhone": "string",
      "createdDate": "string",
      "expiredDate": "string",
      "fee": 1,
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
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `buyerEmail` | string |  |
| `buyerName` | string |  |
| `buyerPhone` | string |  |
| `createdDate` | string |  |
| `expiredDate` | string |  |
| `fee` | number |  |
| `isLocked` | boolean |  |
| `notes` | string |  |
| `paidStatus` | string |  |
| `paymentChannel` | string |  |
| `paymentCode` | string |  |
| `paymentMethod` | string |  |
| `paymentName` | string |  |
| `receiver` | string |  |
| `referenceId` | string |  |
| `relatedId` | number |  |
| `sender` | string |  |
| `sessionId` | string |  |
| `settlementDate` | object |  |
| `status` | number |  |
| `statusDesc` | string |  |
| `subTotal` | number |  |
| `successDate` | object |  |
| `transactionId` | number |  |
| `type` | number |  |
| `typeDesc` | string |  |

## Native endpoint

Through the native iPaymu API, this operation is `POST /transaction` (base URL `https://my.ipaymu.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-transaction.md) for the provider-specific parameters and requirements.

