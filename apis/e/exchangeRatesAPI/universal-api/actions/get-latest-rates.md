# Exchange Rates API: Get Latest Rates

Retrieves latest exchange rates from Exchange Rates API.

```
GET https://connect.mindcloud.co/v1/universal/exchangeRatesAPI/latest/actions/get-latest-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exchange Rates API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exchangeRatesAPI/latest/actions/get-latest-rates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exchangeRatesAPI/latest/actions/get-latest-rates?${params}`, {
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
| `base` | string | no | Optional three-letter currency code for the base currency. Defaults to EUR when omitted. Example: `USD`. |
| `symbols` | string | no | Optional comma-separated currency codes to limit the returned rates, such as USD,CAD,JPY. Accepts multiple values in one string, delimited by `,`. Example: `USD,CAD,JPY`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "rates": {},
      "success": true,
      "timestamp": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base` | string | Base currency code used for the rates. |
| `date` | date | Date for the returned rates. |
| `rates` | object | Map of currency codes to exchange-rate values. |
| `success` | boolean | Whether the latest rates request succeeded. |
| `timestamp` | number | Unix timestamp for when the exchange rates were collected. |

## Native endpoint

Through the native Exchange Rates API API, this operation is `GET latest` (base URL `https://api.exchangeratesapi.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-rates.md) for the provider-specific parameters and requirements.

