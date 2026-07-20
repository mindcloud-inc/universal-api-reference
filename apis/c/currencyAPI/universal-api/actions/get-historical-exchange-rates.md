# CurrencyAPI: Get Historical Exchange Rates

Retrieves historical exchange rates from CurrencyAPI.

```
GET https://connect.mindcloud.co/v1/universal/currencyAPI/latest/actions/get-historical-exchange-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CurrencyAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currencyAPI/latest/actions/get-historical-exchange-rates?connectionId=$CONNECTION_ID&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/currencyAPI/latest/actions/get-historical-exchange-rates?${params}`, {
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
| `date` | string | yes | Historical date in YYYY-MM-DD format. |
| `baseCurrency` | string | no | Base currency for the exchange rates. |
| `currencies` | string | no | Comma-separated currency codes to return. |
| `type` | string | no | Currency type to return: fiat, metal, or crypto. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "lastUpdatedAt": "2026-05-07T12:00:00.000Z",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Quoted currency code |
| `lastUpdatedAt` | date | Provider timestamp for the requested date |
| `value` | number | Historical exchange rate value |

## Native endpoint

Through the native CurrencyAPI API, this operation is `GET /v3/historical` (base URL `https://api.currencyapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-historical-exchange-rates.md) for the provider-specific parameters and requirements.

