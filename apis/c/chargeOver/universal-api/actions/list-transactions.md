# ChargeOver: List Transactions

Retrieves billing transaction records from ChargeOver.

```
GET https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/list-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeOver `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/list-transactions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeOver/latest/actions/list-transactions?${params}`, {
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
      "applied": 1,
      "customer_id": 1,
      "gateway_transid": "string",
      "transaction_date": "string",
      "transaction_id": 1,
      "transaction_method": "string",
      "transaction_status_name": "Ava Chen",
      "transaction_type_name": "Ava Chen",
      "url_self": "https://example.com",
      "void_datetime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `applied` | number |  |
| `customer_id` | number |  |
| `gateway_transid` | string |  |
| `transaction_date` | string |  |
| `transaction_id` | number |  |
| `transaction_method` | string |  |
| `transaction_status_name` | string |  |
| `transaction_type_name` | string |  |
| `url_self` | string |  |
| `void_datetime` | string |  |

## Native endpoint

Through the native ChargeOver API, this operation is `GET /transaction` (base URL `https://{{credentials.siteName}}.chargeover.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transactions.md) for the provider-specific parameters and requirements.

