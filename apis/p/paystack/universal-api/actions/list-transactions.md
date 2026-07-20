# Paystack: List Transactions



```
GET https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paystack `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paystack/latest/actions/list-transactions?${params}`, {
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
      "amount": 1,
      "authorization": {},
      "channel": "string",
      "created_at": "string",
      "currency": "string",
      "customer": {},
      "gateway_response": "string",
      "id": 1,
      "paid_at": "string",
      "reference": "string",
      "requested_amount": 1,
      "status": "string",
      "transaction_date": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `authorization` | object |  |
| `channel` | string |  |
| `created_at` | string |  |
| `currency` | string |  |
| `customer` | object |  |
| `gateway_response` | string |  |
| `id` | number |  |
| `paid_at` | string |  |
| `reference` | string |  |
| `requested_amount` | number |  |
| `status` | string |  |
| `transaction_date` | string |  |

## Native endpoint

Through the native Paystack API, this operation is `GET /transaction` (base URL `https://api.paystack.co`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

