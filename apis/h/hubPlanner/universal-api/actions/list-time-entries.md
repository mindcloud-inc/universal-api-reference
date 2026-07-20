# Hub Planner: List Time Entries

Retrieves time entries from Hub Planner.

```
GET https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/list-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hub Planner `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/list-time-entries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/list-time-entries?${params}`, {
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
      "_id": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "metadata": "string",
      "minutes": 1,
      "project": "string",
      "projectName": "Ava Chen",
      "resource": "string",
      "status": "string",
      "updatedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `createdDate` | date |  |
| `date` | date |  |
| `metadata` | string |  |
| `minutes` | number |  |
| `project` | string |  |
| `projectName` | string |  |
| `resource` | string |  |
| `status` | string |  |
| `updatedDate` | date |  |

## Native endpoint

Through the native Hub Planner API, this operation is `GET /timeentry` (base URL `https://api.hubplanner.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-time-entries.md) for the provider-specific parameters and requirements.

