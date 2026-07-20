# CoinMarketCap: Get Latest Exchange Listings

Retrieves latest exchange listings from CoinMarketCap.

```
GET https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-latest-exchange-listings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinMarketCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-latest-exchange-listings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-latest-exchange-listings?${params}`, {
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
| `limit` | string | no | Maximum number of exchange listings to return. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CoinMarketCap API returns.

## Native endpoint

Through the native CoinMarketCap API, this operation is `GET /v1/exchange/listings/latest` (base URL `https://pro-api.coinmarketcap.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-exchange-listings.md) for the provider-specific parameters and requirements.

