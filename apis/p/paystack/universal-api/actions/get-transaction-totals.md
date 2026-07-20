# Paystack: Get Transaction Totals



```
GET https://connect.mindcloud.co/v1/universal/paystack/latest/actions/get-transaction-totals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paystack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/get-transaction-totals?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paystack/latest/actions/get-transaction-totals?${params}`, {
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
      "pending_transfers": 1,
      "pending_transfers_by_currency": [
        {}
      ],
      "total_transactions": 1,
      "total_volume": 1,
      "total_volume_by_currency": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pending_transfers` | number |  |
| `pending_transfers_by_currency` | array<object> |  |
| `total_transactions` | number |  |
| `total_volume` | number |  |
| `total_volume_by_currency` | array<object> |  |

## Native endpoint

Through the native Paystack API, this operation is `GET /transaction/totals` (base URL `https://api.paystack.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transaction-totals.md) for the provider-specific parameters and requirements.

