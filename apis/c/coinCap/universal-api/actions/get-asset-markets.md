# CoinCap: Get Asset Markets

Retrieves markets for an asset from CoinCap.

```
GET https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/get-asset-markets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinCap `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/get-asset-markets?connectionId=$CONNECTION_ID&limit=25&offset=0&slug=bitcoin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "slug": "bitcoin"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/get-asset-markets?${params}`, {
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
| `slug` | string | yes | The asset slug to retrieve markets for. Example: `bitcoin`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "baseId": "string",
      "baseSymbol": "string",
      "exchangeId": "string",
      "priceUsd": "string",
      "quoteId": "string",
      "quoteSymbol": "string",
      "volumePercent": "string",
      "volumeUsd24Hr": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `baseId` | string |  |
| `baseSymbol` | string |  |
| `exchangeId` | string |  |
| `priceUsd` | string |  |
| `quoteId` | string |  |
| `quoteSymbol` | string |  |
| `volumePercent` | string |  |
| `volumeUsd24Hr` | string |  |

## Native endpoint

Through the native CoinCap API, this operation is `GET /assets/:slug/markets` (base URL `https://rest.coincap.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-asset-markets.md) for the provider-specific parameters and requirements.

