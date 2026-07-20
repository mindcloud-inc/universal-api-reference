# Fixer: Get Time Series Rates

Retrieves time-series exchange rates from Fixer.

```
GET https://connect.mindcloud.co/v1/universal/fixer/latest/actions/get-time-series-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fixer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fixer/latest/actions/get-time-series-rates?connectionId=$CONNECTION_ID&startDate=YYYY-MM-DD&endDate=YYYY-MM-DD" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "startDate": "YYYY-MM-DD",
  "endDate": "YYYY-MM-DD"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fixer/latest/actions/get-time-series-rates?${params}`, {
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
| `startDate` | string | yes | Start date in YYYY-MM-DD format. Example: `YYYY-MM-DD`. |
| `endDate` | string | yes | End date in YYYY-MM-DD format. Example: `YYYY-MM-DD`. |
| `symbols` | string | no | Optional comma-separated list of currency codes to limit the returned rates. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `base` | string | no | Optional three-letter base currency code. Fixer defaults to EUR and some plans restrict custom base currencies. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "date": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Three-letter ISO currency code. |
| `date` | string | Rate date in YYYY-MM-DD format. |
| `value` | number | Exchange rate for that date and code. |

## Native endpoint

Through the native Fixer API, this operation is `GET /timeseries` (base URL `https://data.fixer.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-series-rates.md) for the provider-specific parameters and requirements.

