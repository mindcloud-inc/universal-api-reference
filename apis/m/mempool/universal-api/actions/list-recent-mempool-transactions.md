# Mempool: List Recent Mempool Transactions

Retrieves recent mempool transactions from Mempool.

```
GET https://connect.mindcloud.co/v1/universal/mempool/latest/actions/list-recent-mempool-transactions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mempool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mempool/latest/actions/list-recent-mempool-transactions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mempool/latest/actions/list-recent-mempool-transactions?${params}`, {
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
      "fee": 1,
      "txid": "string",
      "value": 1,
      "vsize": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fee` | number |  |
| `txid` | string |  |
| `value` | number |  |
| `vsize` | number |  |

## Native endpoint

Through the native Mempool API, this operation is `GET /mempool/recent` (base URL `https://mempool.space/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recent-mempool-transactions.md) for the provider-specific parameters and requirements.

