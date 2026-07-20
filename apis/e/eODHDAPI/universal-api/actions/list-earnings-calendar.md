# EODHD: List Earnings Calendar

Retrieves earnings calendar events from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-earnings-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-earnings-calendar?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-earnings-calendar?${params}`, {
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
| `symbols` | string | no | Comma-separated EODHD tickers. When supplied, from/to are ignored by EODHD. |
| `from` | date | no | Start date in `YYYY-MM-DD` format. Example: `2025-01-01`. |
| `to` | date | no | End date in `YYYY-MM-DD` format. Example: `2025-12-31`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actual": 1,
      "before_after_market": "string",
      "code": "string",
      "currency": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "difference": 1,
      "estimate": 1,
      "percent": 1,
      "report_date": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actual` | number | Actual reported value. |
| `before_after_market` | string | Before/after-market marker. |
| `code` | string | Ticker code. |
| `currency` | string | Currency code. |
| `date` | date | Event date. |
| `difference` | number | Actual-estimate difference. |
| `estimate` | number | Estimated value. |
| `percent` | number | Difference percentage. |
| `report_date` | date | Earnings report date. |

## Native endpoint

Through the native EODHD API, this operation is `GET /calendar/earnings` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-earnings-calendar.md) for the provider-specific parameters and requirements.

