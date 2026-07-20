# Finnhub: List IPO Calendar

Retrieves the IPO calendar from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-ipo-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-ipo-calendar?connectionId=$CONNECTION_ID&from=2026-04-01&to=2026-04-30" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "2026-04-01",
  "to": "2026-04-30"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/list-ipo-calendar?${params}`, {
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
| `from` | string | yes | Start date in YYYY-MM-DD format. Example: `2026-04-01`. |
| `to` | string | yes | End date in YYYY-MM-DD format. Example: `2026-04-30`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ipoCalendar": {
        "date": "2026-05-07T12:00:00.000Z",
        "exchange": "string",
        "name": "Ava Chen",
        "numberOfShares": 1,
        "price": "string",
        "status": "string",
        "symbol": "string",
        "totalSharesValue": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ipoCalendar` | array<object> |  |
| `ipoCalendar.date` | date |  |
| `ipoCalendar.exchange` | string |  |
| `ipoCalendar.name` | string |  |
| `ipoCalendar.numberOfShares` | number |  |
| `ipoCalendar.price` | string |  |
| `ipoCalendar.status` | string |  |
| `ipoCalendar.symbol` | string |  |
| `ipoCalendar.totalSharesValue` | number |  |

## Native endpoint

Through the native Finnhub API, this operation is `GET /calendar/ipo` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ipo-calendar.md) for the provider-specific parameters and requirements.

