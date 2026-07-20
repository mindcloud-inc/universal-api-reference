# Timewax: List Changed Projects

Retrieves changed projects from Timewax by date range.

```
GET https://connect.mindcloud.co/v1/universal/timewax/latest/actions/list-changed-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timewax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timewax/latest/actions/list-changed-projects?connectionId=$CONNECTION_ID&request.dateFrom=2026-05-07T12%3A00%3A00.000Z&request.dateTo=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "request.dateFrom": "2026-05-07T12:00:00.000Z",
  "request.dateTo": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timewax/latest/actions/list-changed-projects?${params}`, {
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
| `request.dateFrom` | date | yes | Required. Add or modification date from, format yyyymmdd or yyyy-mm-dd. |
| `request.dateTo` | date | yes | Required. Add or modification date to, format yyyymmdd or yyyy-mm-dd. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "modifyDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Project code. |
| `modifyDate` | date | Last modification date. |
| `name` | string | Project name. |

## Native endpoint

Through the native Timewax API, this operation is `POST project/list_changed/` (base URL `https://api.timewax.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-changed-projects.md) for the provider-specific parameters and requirements.

