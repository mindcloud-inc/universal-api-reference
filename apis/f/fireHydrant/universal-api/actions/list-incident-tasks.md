# FireHydrant: List Incident Tasks

Retrieves incident tasks from FireHydrant.

```
GET https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-incident-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FireHydrant `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-incident-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0&incidentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "incidentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-incident-tasks?${params}`, {
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
| `incidentId` | string | yes | The FireHydrant incident ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "assignee": {},
          "createdAt": "2026-05-07T12:00:00.000Z",
          "createdBy": {},
          "description": "string",
          "dueAt": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "state": "string",
          "title": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "pagination": {
        "count": 1,
        "items": 1,
        "last": 1,
        "page": 1,
        "pages": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].assignee` | object |  |
| `data[].createdAt` | date |  |
| `data[].createdBy` | object |  |
| `data[].description` | string |  |
| `data[].dueAt` | date |  |
| `data[].id` | string |  |
| `data[].state` | string |  |
| `data[].title` | string |  |
| `data[].updatedAt` | date |  |
| `pagination.count` | number |  |
| `pagination.items` | number |  |
| `pagination.last` | number |  |
| `pagination.page` | number |  |
| `pagination.pages` | number |  |

## Native endpoint

Through the native FireHydrant API, this operation is `GET /incidents/:incident_id/tasks` (base URL `https://api.firehydrant.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-incident-tasks.md) for the provider-specific parameters and requirements.

