# Gift Up: List Report Transactions



```
GET https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/list-report-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gift Up `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/list-report-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giftUp/latest/actions/list-report-transactions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "eventOccuredAtLocationId": "string",
      "eventOccuredOn": "2026-05-07T12:00:00.000Z",
      "eventType": "string",
      "giftCard": {},
      "giftUpFee": 1,
      "id": "string",
      "metadata": {},
      "orderDetails": {},
      "orderId": "string",
      "reason": "string",
      "referrer": "string",
      "whoEmail": "ava@example.com",
      "whoName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `eventOccuredAtLocationId` | string |  |
| `eventOccuredOn` | date |  |
| `eventType` | string |  |
| `giftCard` | object |  |
| `giftUpFee` | number |  |
| `id` | string |  |
| `metadata` | object |  |
| `orderDetails` | object |  |
| `orderId` | string |  |
| `reason` | string |  |
| `referrer` | string |  |
| `whoEmail` | string |  |
| `whoName` | string |  |

## Native endpoint

Through the native Gift Up API, this operation is `GET /reports/transactions` (base URL `https://api.giftup.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-report-transactions.md) for the provider-specific parameters and requirements.

