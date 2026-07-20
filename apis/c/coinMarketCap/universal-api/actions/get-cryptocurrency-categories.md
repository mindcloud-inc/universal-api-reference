# CoinMarketCap: Get Cryptocurrency Categories

Retrieves cryptocurrency categories from CoinMarketCap.

```
GET https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-cryptocurrency-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinMarketCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-cryptocurrency-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-cryptocurrency-categories?${params}`, {
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
| `limit` | string | no | Maximum number of categories to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avg_price_change": 1,
      "description": "string",
      "id": "string",
      "last_updated": "2026-05-07T12:00:00.000Z",
      "market_cap": 1,
      "market_cap_change": 1,
      "name": "Ava Chen",
      "num_tokens": 1,
      "title": "string",
      "volume": 1,
      "volume_change": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avg_price_change` | number |  |
| `description` | string |  |
| `id` | string |  |
| `last_updated` | date |  |
| `market_cap` | number |  |
| `market_cap_change` | number |  |
| `name` | string |  |
| `num_tokens` | number |  |
| `title` | string |  |
| `volume` | number |  |
| `volume_change` | number |  |

## Native endpoint

Through the native CoinMarketCap API, this operation is `GET /v1/cryptocurrency/categories` (base URL `https://pro-api.coinmarketcap.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cryptocurrency-categories.md) for the provider-specific parameters and requirements.

