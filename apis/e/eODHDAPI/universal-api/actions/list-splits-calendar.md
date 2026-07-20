# EODHD: List Splits Calendar

Retrieves stock split calendar events from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-splits-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-splits-calendar?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-splits-calendar?${params}`, {
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
| `from` | date | no | Start date in YYYY-MM-DD format. Example: `2025-01-01`. |
| `to` | date | no | End date in YYYY-MM-DD format. Example: `2025-12-31`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "exchange": "string",
      "newShares": 1,
      "oldShares": 1,
      "split": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Ticker code. |
| `date` | date | Split date. |
| `exchange` | string | Exchange code. |
| `newShares` | number | New share count. |
| `oldShares` | number | Old share count. |
| `split` | string | Split ratio. |

## Native endpoint

Through the native EODHD API, this operation is `GET /calendar/splits` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-splits-calendar.md) for the provider-specific parameters and requirements.

