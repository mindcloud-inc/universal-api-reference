# Timewax: List Planning Bookings

Retrieves planning booking records from Timewax.

```
GET https://connect.mindcloud.co/v1/universal/timewax/latest/actions/list-planning-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timewax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timewax/latest/actions/list-planning-bookings?connectionId=$CONNECTION_ID&request.dateFrom=2026-05-07T12%3A00%3A00.000Z&request.dateTo=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request.dateFrom": "2026-05-07T12:00:00.000Z",
  "request.dateTo": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timewax/latest/actions/list-planning-bookings?${params}`, {
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
| `request.dateFrom` | date | yes | Required. Date from, format yyyymmdd or yyyy-mm-dd. |
| `request.dateTo` | date | yes | Required. Date to, format yyyymmdd or yyyy-mm-dd. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "entryId": "string",
      "hours": 1,
      "project": "string",
      "resource": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Planning booking date. |
| `entryId` | string | Planning booking identifier. |
| `hours` | number | Booked hours. |
| `project` | string | Associated project. |
| `resource` | string | Assigned resource. |

## Native endpoint

Through the native Timewax API, this operation is `POST calendar/entries/list/` (base URL `https://api.timewax.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-planning-bookings.md) for the provider-specific parameters and requirements.

