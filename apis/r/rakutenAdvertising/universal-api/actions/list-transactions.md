# Rakuten Advertising: List transactions

Retrieves transactions from Rakuten Advertising.

```
GET https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rakuten Advertising `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/list-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/list-transactions?${params}`, {
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
      "advertiserId": "string",
      "amount": 1,
      "commission": 1,
      "currency": "string",
      "orderId": "string",
      "processDate": "2026-05-07T12:00:00.000Z",
      "sku": "string",
      "transactionDate": "2026-05-07T12:00:00.000Z",
      "transactionId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `advertiserId` | string |  |
| `amount` | number |  |
| `commission` | number |  |
| `currency` | string |  |
| `orderId` | string |  |
| `processDate` | date |  |
| `sku` | string |  |
| `transactionDate` | date |  |
| `transactionId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Rakuten Advertising API, this operation is `GET /events/1.0/transactions` (base URL `https://api.linksynergy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

