# Currencylayer: Convert Currency Amount Using Historical Rates

Converts a currency amount using historical Currencylayer rates.

```
GET https://connect.mindcloud.co/v1/universal/currencylayer/latest/actions/convert-currency-amount-using-historical-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Currencylayer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currencylayer/latest/actions/convert-currency-amount-using-historical-rates?connectionId=$CONNECTION_ID&fromCurrency=string&toCurrency=string&amount=1&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromCurrency": "string",
  "toCurrency": "string",
  "amount": "1",
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/currencylayer/latest/actions/convert-currency-amount-using-historical-rates?${params}`, {
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
| `fromCurrency` | string | yes | 3-letter currency code to convert from. |
| `toCurrency` | string | yes | 3-letter currency code to convert to. |
| `amount` | number | yes | Amount to convert. |
| `date` | string | yes | Historical conversion date in YYYY-MM-DD format. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Currencylayer API returns.

## Native endpoint

Through the native Currencylayer API, this operation is `GET /convert` (base URL `https://api.currencylayer.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-currency-amount-using-historical-rates.md) for the provider-specific parameters and requirements.

