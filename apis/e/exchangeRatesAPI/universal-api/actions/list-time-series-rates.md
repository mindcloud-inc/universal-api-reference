# Exchange Rates API: List Time Series Rates

Retrieves time-series exchange rates from Exchange Rates API.

```
GET https://connect.mindcloud.co/v1/universal/exchangeRatesAPI/latest/actions/list-time-series-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exchange Rates API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exchangeRatesAPI/latest/actions/list-time-series-rates?connectionId=$CONNECTION_ID&startDate=2024-01-01&endDate=2024-01-31" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "2024-01-01",
  "endDate": "2024-01-31"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exchangeRatesAPI/latest/actions/list-time-series-rates?${params}`, {
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
| `startDate` | date | yes | Start date of the time frame in YYYY-MM-DD format. Example: `2024-01-01`. |
| `endDate` | date | yes | End date of the time frame in YYYY-MM-DD format. Example: `2024-01-31`. |
| `base` | string | no | Optional three-letter currency code for the base currency. Defaults to EUR when omitted. Example: `USD`. |
| `symbols` | string | no | Optional comma-separated currency codes to limit the returned rates, such as USD,CAD,JPY. Accepts multiple values in one string, delimited by `,`. Example: `USD,CAD,JPY`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "base": "string",
      "end_date": "2026-05-07T12:00:00.000Z",
      "rates": {},
      "start_date": "2026-05-07T12:00:00.000Z",
      "success": true,
      "timeseries": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `base` | string | Base currency code used for the rates. |
| `end_date` | date | End date of the returned time frame. |
| `rates` | object | Map of dates to currency exchange-rate values. |
| `start_date` | date | Start date of the returned time frame. |
| `success` | boolean | Whether the time-series request succeeded. |
| `timeseries` | boolean | Whether the response is from the time-series endpoint. |

## Native endpoint

Through the native Exchange Rates API API, this operation is `GET timeseries` (base URL `https://api.exchangeratesapi.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-series-rates.md) for the provider-specific parameters and requirements.

