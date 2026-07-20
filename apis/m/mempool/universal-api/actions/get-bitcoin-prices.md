# Mempool: Get Bitcoin Prices

Retrieves Bitcoin price data from Mempool.

```
GET https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-bitcoin-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mempool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-bitcoin-prices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-bitcoin-prices?${params}`, {
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
      "AUD": 1,
      "CAD": 1,
      "CHF": 1,
      "EUR": 1,
      "GBP": 1,
      "JPY": 1,
      "time": 1,
      "USD": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AUD` | number |  |
| `CAD` | number |  |
| `CHF` | number |  |
| `EUR` | number |  |
| `GBP` | number |  |
| `JPY` | number |  |
| `time` | number |  |
| `USD` | number |  |

## Native endpoint

Through the native Mempool API, this operation is `GET /v1/prices` (base URL `https://mempool.space/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bitcoin-prices.md) for the provider-specific parameters and requirements.

