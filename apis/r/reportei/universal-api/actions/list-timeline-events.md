# Reportei: List Timeline Events

Retrieves timeline events from Reportei.

```
GET https://connect.mindcloud.co/v1/universal/reportei/latest/actions/list-timeline-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reportei `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reportei/latest/actions/list-timeline-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reportei/latest/actions/list-timeline-events?${params}`, {
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
| `projectId` | number | no | Filtrar por projeto. |
| `reportId` | number | no | Filtrar por relatório. |
| `date` | date | no | Filtrar por data. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "date": "string",
          "id": 1,
          "title": "string"
        }
      ],
      "meta": {
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].date` | string | Timeline event date |
| `data[].id` | number | Timeline event identifier |
| `data[].title` | string | Timeline event title |
| `meta.total` | number | Total number of timeline events |

## Native endpoint

Through the native Reportei API, this operation is `GET /timeline-events` (base URL `https://app.reportei.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-timeline-events.md) for the provider-specific parameters and requirements.

