# CoinMarketCap: Get Exchange Map

Retrieves exchange IDs and slugs from CoinMarketCap.

```
GET https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-exchange-map
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinMarketCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-exchange-map?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-exchange-map?${params}`, {
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
| `slug` | string | no | Exchange slug, for example binance. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "first_historical_data": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_active": 1,
      "is_listed": 1,
      "is_redistributable": 1,
      "last_historical_data": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "slug": "string"
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
| `is_listed` | number |  |
| `is_redistributable` | number |  |
| `last_historical_data` | date |  |
| `name` | string |  |
| `slug` | string |  |

## Native endpoint

Through the native CoinMarketCap API, this operation is `GET /v1/exchange/map` (base URL `https://pro-api.coinmarketcap.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-exchange-map.md) for the provider-specific parameters and requirements.

