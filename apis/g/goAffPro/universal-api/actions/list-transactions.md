# GoAffPro: List Transactions

Retrieves transaction log entries from GoAffPro.

```
GET https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoAffPro `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goAffPro/latest/actions/list-transactions?${params}`, {
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
| `affiliateId` | string | no | Only return transactions for this affiliate ID. |
| `type` | string | no | Only return transactions for this entity type. |
| `isPaid` | boolean | no | Only return transactions by payment status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "affiliateId": 1,
      "amount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "endingBalance": 1,
      "entityId": "string",
      "entityType": "string",
      "eventType": "string",
      "isPaid": true,
      "startingBalance": 1,
      "txId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `affiliateId` | number |  |
| `amount` | number |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `endingBalance` | number |  |
| `entityId` | string |  |
| `entityType` | string |  |
| `eventType` | string |  |
| `isPaid` | boolean |  |
| `startingBalance` | number |  |
| `txId` | number |  |

## Native endpoint

Through the native GoAffPro API, this operation is `GET /admin/transactions` (base URL `https://api.goaffpro.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

