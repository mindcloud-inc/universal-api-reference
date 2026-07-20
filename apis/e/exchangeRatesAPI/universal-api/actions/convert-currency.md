# Exchange Rates API: Convert Currency

Converts an amount between currencies in Exchange Rates API.

```
GET https://connect.mindcloud.co/v1/universal/exchangeRatesAPI/latest/actions/convert-currency
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exchange Rates API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exchangeRatesAPI/latest/actions/convert-currency?connectionId=$CONNECTION_ID&from=USD&to=EUR&amount=25" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "USD",
  "to": "EUR",
  "amount": "25"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exchangeRatesAPI/latest/actions/convert-currency?${params}`, {
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
| `from` | string | yes | Three-letter currency code to convert from. Example: `USD`. |
| `to` | string | yes | Three-letter currency code to convert to. Example: `EUR`. |
| `amount` | number | yes | Amount to convert. Example: `25`. |
| `date` | date | no | Optional historical conversion date in YYYY-MM-DD format. Example: `2024-01-15`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "historical": true,
      "info": {},
      "query": {},
      "result": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Date for the conversion rate data. |
| `historical` | boolean | Whether historical rates were used for this conversion. |
| `info` | object | Conversion rate metadata including timestamp and rate. |
| `query` | object | Conversion query details including from currency, to currency, and amount. |
| `result` | number | Converted amount result. |
| `success` | boolean | Whether the conversion request succeeded. |

## Native endpoint

Through the native Exchange Rates API API, this operation is `GET convert` (base URL `https://api.exchangeratesapi.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-currency.md) for the provider-specific parameters and requirements.

