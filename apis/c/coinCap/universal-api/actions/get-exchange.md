# CoinCap: Get Exchange

Retrieves an exchange from CoinCap.

```
GET https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/get-exchange
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/get-exchange?connectionId=$CONNECTION_ID&exchange=binance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "exchange": "binance"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/get-exchange?${params}`, {
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
| `exchange` | string | yes | The exchange ID to retrieve. Example: `binance`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "exchangeId": "string",
      "exchangeUrl": "https://example.com",
      "name": "Ava Chen",
      "percentTotalVolume": "string",
      "rank": "string",
      "socket": true,
      "tradingPairs": "string",
      "updated": 1,
      "volumeUsd": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `exchangeId` | string |  |
| `exchangeUrl` | string |  |
| `name` | string |  |
| `percentTotalVolume` | string |  |
| `rank` | string |  |
| `socket` | boolean |  |
| `tradingPairs` | string |  |
| `updated` | number |  |
| `volumeUsd` | string |  |

## Native endpoint

Through the native CoinCap API, this operation is `GET /exchanges/:exchange` (base URL `https://rest.coincap.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-exchange.md) for the provider-specific parameters and requirements.

