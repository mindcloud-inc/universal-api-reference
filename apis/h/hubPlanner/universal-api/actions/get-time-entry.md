# Hub Planner: Get Time Entry

Retrieves a time entry from Hub Planner.

```
GET https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/get-time-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hub Planner `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/get-time-entry?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubPlanner/latest/actions/get-time-entry?${params}`, {
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
| `id` | string | yes | Hub Planner time entry ID from the _id field. |

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

Through the native Hub Planner API, this operation is `GET /timeentry/:id` (base URL `https://api.hubplanner.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-entry.md) for the provider-specific parameters and requirements.

