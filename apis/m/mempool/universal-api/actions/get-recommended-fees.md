# Mempool: Get Recommended Fees

Retrieves recommended transaction fees from Mempool.

```
GET https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-recommended-fees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mempool `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-recommended-fees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mempool/latest/actions/get-recommended-fees?${params}`, {
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
      "economyFee": 1,
      "fastestFee": 1,
      "halfHourFee": 1,
      "hourFee": 1,
      "minimumFee": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `economyFee` | number |  |
| `fastestFee` | number |  |
| `halfHourFee` | number |  |
| `hourFee` | number |  |
| `minimumFee` | number |  |

## Native endpoint

Through the native Mempool API, this operation is `GET /v1/fees/recommended` (base URL `https://mempool.space/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recommended-fees.md) for the provider-specific parameters and requirements.

