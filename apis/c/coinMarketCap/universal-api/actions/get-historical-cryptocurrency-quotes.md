# CoinMarketCap: Get Historical Cryptocurrency Quotes

Retrieves historical cryptocurrency quotes from CoinMarketCap.

```
GET https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-historical-cryptocurrency-quotes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinMarketCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-historical-cryptocurrency-quotes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-historical-cryptocurrency-quotes?${params}`, {
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
| `id` | string | no | CoinMarketCap cryptocurrency ID, for example 1. |
| `interval` | string | no | Historical interval such as daily. |
| `timeEnd` | string | no | End date or timestamp for the historical window. |
| `timeStart` | string | no | Start date or timestamp for the historical window. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native CoinMarketCap API returns.

## Native endpoint

Through the native CoinMarketCap API, this operation is `GET /v3/cryptocurrency/quotes/historical` (base URL `https://pro-api.coinmarketcap.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-historical-cryptocurrency-quotes.md) for the provider-specific parameters and requirements.

