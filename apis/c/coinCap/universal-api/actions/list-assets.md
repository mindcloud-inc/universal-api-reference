# CoinCap: List Assets

Retrieves assets from CoinCap.

```
GET https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/list-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinCap `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/list-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinCap/latest/actions/list-assets?${params}`, {
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
| `search` | string | no | Search by asset slug or symbol. Example: `bitcoin`. |
| `ids` | string | no | Comma-separated asset IDs to include. Example: `bitcoin,ethereum`. |

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

Through the native CoinCap API, this operation is `GET /assets` (base URL `https://rest.coincap.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-assets.md) for the provider-specific parameters and requirements.

