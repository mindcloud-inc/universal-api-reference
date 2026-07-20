# EODHD: List Economic Events

Retrieves economic events from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-economic-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-economic-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-economic-events?${params}`, {
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
| `country` | string | no | Country code filter, for example US. Example: `US`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `comparison` | string | no | Optional economic-event comparison filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actual": 1,
      "change": 1,
      "changePercentage": 1,
      "country": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "estimate": 1,
      "event": "string",
      "impact": "string",
      "previous": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actual` | number | Actual value. |
| `change` | number | Absolute change. |
| `changePercentage` | number | Change percentage. |
| `country` | string | Country code. |
| `date` | date | Event date. |
| `estimate` | number | Estimated value. |
| `event` | string | Economic event name. |
| `impact` | string | Impact value. |
| `previous` | number | Previous value. |

## Native endpoint

Through the native EODHD API, this operation is `GET /economic-events` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-economic-events.md) for the provider-specific parameters and requirements.

