# CoinCap: Get Asset

Retrieves an asset from CoinCap.

```
GET https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/get-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/get-asset?connectionId=$CONNECTION_ID&slug=bitcoin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "bitcoin"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/get-asset?${params}`, {
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
| `slug` | string | yes | The asset slug to retrieve. Example: `bitcoin`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changePercent24Hr": "string",
      "explorer": "string",
      "id": "string",
      "marketCapUsd": "string",
      "maxSupply": "string",
      "name": "Ava Chen",
      "priceUsd": "string",
      "rank": "string",
      "supply": "string",
      "symbol": "string",
      "tokens": {},
      "volumeUsd24Hr": "string",
      "vwap24Hr": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changePercent24Hr` | string |  |
| `explorer` | string |  |
| `id` | string |  |
| `marketCapUsd` | string |  |
| `maxSupply` | string |  |
| `name` | string |  |
| `priceUsd` | string |  |
| `rank` | string |  |
| `supply` | string |  |
| `symbol` | string |  |
| `tokens` | object |  |
| `volumeUsd24Hr` | string |  |
| `vwap24Hr` | string |  |

## Native endpoint

Through the native CoinCap API, this operation is `GET /assets/:slug` (base URL `https://rest.coincap.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset.md) for the provider-specific parameters and requirements.

