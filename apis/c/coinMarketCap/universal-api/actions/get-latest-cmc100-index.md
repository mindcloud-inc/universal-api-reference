# CoinMarketCap: Get Latest CMC100 Index

Retrieves the latest CMC100 index value from CoinMarketCap.

```
GET https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-latest-cmc100-index
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinMarketCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-latest-cmc100-index?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-latest-cmc100-index?${params}`, {
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
      "constituents": [
        {
          "id": 1,
          "name": "Ava Chen",
          "symbol": "string",
          "url": "https://example.com",
          "weight": 1
        }
      ],
      "last_update": "2026-05-07T12:00:00.000Z",
      "next_update": "2026-05-07T12:00:00.000Z",
      "value": 1,
      "value_24h_percentage_change": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `constituents[].id` | number |  |
| `constituents[].name` | string |  |
| `constituents[].symbol` | string |  |
| `constituents[].url` | string |  |
| `constituents[].weight` | number |  |
| `last_update` | date |  |
| `next_update` | date |  |
| `value` | number |  |
| `value_24h_percentage_change` | number |  |

## Native endpoint

Through the native CoinMarketCap API, this operation is `GET /v3/index/cmc100-latest` (base URL `https://pro-api.coinmarketcap.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-cmc100-index.md) for the provider-specific parameters and requirements.

