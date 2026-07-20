# ServiceM8: List Tasks



```
GET https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceM8 `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/list-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/serviceM8/latest/actions/list-tasks?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "assignedToStaffUuid": "string",
      "completedByStaffUuid": "string",
      "completedTimestamp": "2026-05-07T12:00:00.000Z",
      "createDate": "2026-05-07T12:00:00.000Z",
      "createdByStaffUuid": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "editDate": "2026-05-07T12:00:00.000Z",
      "lat": 1,
      "lng": 1,
      "name": "Ava Chen",
      "relatedObject": "string",
      "relatedObjectUuid": "string",
      "taskComplete": "string",
      "taskDetails": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number |  |
| `assignedToStaffUuid` | string |  |
| `completedByStaffUuid` | string |  |
| `completedTimestamp` | date |  |
| `createDate` | date |  |
| `createdByStaffUuid` | string |  |
| `dueDate` | date |  |
| `editDate` | date |  |
| `lat` | number |  |
| `lng` | number |  |
| `name` | string |  |
| `relatedObject` | string |  |
| `relatedObjectUuid` | string |  |
| `taskComplete` | string |  |
| `taskDetails` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native ServiceM8 API, this operation is `GET /api_1.0/task.json` (base URL `https://api.servicem8.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

