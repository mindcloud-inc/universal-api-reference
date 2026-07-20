# CoinCap: List Exchanges

Retrieves exchanges from CoinCap.

```
GET https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/list-exchanges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinCap `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/list-exchanges?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/list-exchanges?${params}`, {
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

Through the native CoinCap API, this operation is `GET /exchanges` (base URL `https://rest.coincap.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-exchanges.md) for the provider-specific parameters and requirements.

