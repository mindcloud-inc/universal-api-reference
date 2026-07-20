# CoinMarketCap: Get Cryptocurrency Map

Retrieves cryptocurrency IDs and symbols from CoinMarketCap.

```
GET https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-cryptocurrency-map
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinMarketCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-cryptocurrency-map?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-cryptocurrency-map?${params}`, {
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
| `slug` | string | no | Cryptocurrency slug filter, for example bitcoin. |
| `symbol` | string | no | Cryptocurrency symbol filter, for example BTC. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "first_historical_data": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_active": 1,
      "last_historical_data": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "platform": {
        "id": 1,
        "name": "Ava Chen",
        "slug": "string",
        "symbol": "string",
        "token_address": "string"
      },
      "rank": 1,
      "slug": "string",
      "status": 1,
      "symbol": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `first_historical_data` | date |  |
| `id` | number |  |
| `is_active` | number |  |
| `last_historical_data` | date |  |
| `name` | string |  |
| `platform.id` | number |  |
| `platform.name` | string |  |
| `platform.slug` | string |  |
| `platform.symbol` | string |  |
| `platform.token_address` | string |  |
| `rank` | number |  |
| `slug` | string |  |
| `status` | number |  |
| `symbol` | string |  |

## Native endpoint

Through the native CoinMarketCap API, this operation is `GET /v1/cryptocurrency/map` (base URL `https://pro-api.coinmarketcap.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cryptocurrency-map.md) for the provider-specific parameters and requirements.

