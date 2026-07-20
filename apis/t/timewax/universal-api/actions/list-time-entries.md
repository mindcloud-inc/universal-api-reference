# Timewax: List Time Entries

Retrieves time entry records from Timewax.

```
GET https://connect.mindcloud.co/v1/universal/timewax/latest/actions/list-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timewax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timewax/latest/actions/list-time-entries?connectionId=$CONNECTION_ID&request.dateFrom=2026-05-07T12%3A00%3A00.000Z&request.dateTo=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request.dateFrom": "2026-05-07T12:00:00.000Z",
  "request.dateTo": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timewax/latest/actions/list-time-entries?${params}`, {
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
      "hours": 1,
      "id": "string",
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
| `date` | date | Time entry date. |
| `hours` | number | Logged hours. |
| `id` | string | Time entry identifier. |
| `project` | string | Associated project. |
| `resource` | string | Resource that logged time. |

## Native endpoint

Through the native Timewax API, this operation is `POST time/entries/list/` (base URL `https://api.timewax.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-entries.md) for the provider-specific parameters and requirements.

