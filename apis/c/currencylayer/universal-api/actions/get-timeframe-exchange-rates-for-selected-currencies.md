# Currencylayer: Get Timeframe Exchange Rates For Selected Currencies

Retrieves timeframe exchange rates for selected currencies from Currencylayer.

```
GET https://connect.mindcloud.co/v1/universal/currencylayer/latest/actions/get-timeframe-exchange-rates-for-selected-currencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Currencylayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currencylayer/latest/actions/get-timeframe-exchange-rates-for-selected-currencies?connectionId=$CONNECTION_ID&startDate=string&endDate=string&currencies=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "string",
  "endDate": "string",
  "currencies": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/currencylayer/latest/actions/get-timeframe-exchange-rates-for-selected-currencies?${params}`, {
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
| `startDate` | string | yes | Start date for the requested timeframe, in YYYY-MM-DD format. |
| `endDate` | string | yes | End date for the requested timeframe, in YYYY-MM-DD format. |
| `currencies` | string | yes | Comma-separated 3-letter currency codes to limit the returned rates. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Currencylayer API returns.

## Native endpoint

Through the native Currencylayer API, this operation is `GET /timeframe` (base URL `https://api.currencylayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-timeframe-exchange-rates-for-selected-currencies.md) for the provider-specific parameters and requirements.

