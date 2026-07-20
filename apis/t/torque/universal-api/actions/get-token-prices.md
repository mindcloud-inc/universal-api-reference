# Torque: Get Token Prices



```
GET https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-token-prices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Torque `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-token-prices?connectionId=$CONNECTION_ID&symbols=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbols": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/torque/latest/actions/get-token-prices?${params}`, {
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
| `symbols` | string | yes | Comma-separated token symbols. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "fullyDilutedValuation": 1,
      "lastUpdated": "2026-05-07T12:00:00.000Z",
      "marketCap": 1,
      "price": 1,
      "priceChange24h": 1,
      "priceChange7d": 1,
      "source": "string",
      "symbol": "string",
      "totalVolume24h": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `fullyDilutedValuation` | number |  |
| `lastUpdated` | date |  |
| `marketCap` | number |  |
| `price` | number |  |
| `priceChange24h` | number |  |
| `priceChange7d` | number |  |
| `source` | string |  |
| `symbol` | string |  |
| `totalVolume24h` | number |  |

## Native endpoint

Through the native Torque API, this operation is `GET /token-prices` (base URL `https://app.torque.fi/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-token-prices.md) for the provider-specific parameters and requirements.

