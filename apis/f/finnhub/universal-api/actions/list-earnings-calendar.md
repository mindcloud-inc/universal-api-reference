# Finnhub: List Earnings Calendar

Retrieves the earnings calendar from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-earnings-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-earnings-calendar?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-earnings-calendar?${params}`, {
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
| `from` | string | no | Start date in YYYY-MM-DD format. Example: `2026-04-01`. |
| `to` | string | no | End date in YYYY-MM-DD format. Example: `2026-04-30`. |
| `symbol` | string | no | Optional company symbol, such as AAPL. Example: `e.g. AAPL`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `international` | boolean | no | Set true to include international earnings calendar entries. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "earningsCalendar": {
        "date": "2026-05-07T12:00:00.000Z",
        "epsActual": 1,
        "epsEstimate": 1,
        "hour": "string",
        "quarter": 1,
        "revenueActual": 1,
        "revenueEstimate": 1,
        "symbol": "string",
        "year": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `earningsCalendar` | array<object> |  |
| `earningsCalendar.date` | date |  |
| `earningsCalendar.epsActual` | number |  |
| `earningsCalendar.epsEstimate` | number |  |
| `earningsCalendar.hour` | string |  |
| `earningsCalendar.quarter` | number |  |
| `earningsCalendar.revenueActual` | number |  |
| `earningsCalendar.revenueEstimate` | number |  |
| `earningsCalendar.symbol` | string |  |
| `earningsCalendar.year` | number |  |

## Native endpoint

Through the native Finnhub API, this operation is `GET /calendar/earnings` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-earnings-calendar.md) for the provider-specific parameters and requirements.

