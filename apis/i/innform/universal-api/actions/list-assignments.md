# Innform: List Assignments

Retrieves assignments from Innform.

```
GET https://connect.mindcloud.co/v1/universal/innform/latest/actions/list-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Innform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/innform/latest/actions/list-assignments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/innform/latest/actions/list-assignments?${params}`, {
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
| `status` | string | no | Optional assignment status filter. One of: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedAt": "2026-05-07T12:00:00.000Z",
      "completedAt": "2026-05-07T12:00:00.000Z",
      "course": {},
      "dueDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "result": 1,
      "score": 1,
      "status": "string",
      "url": "https://example.com",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedAt` | date | When the assignment was created. |
| `completedAt` | date | When the assignment was completed. |
| `course` | object | Assigned training item summary. |
| `dueDate` | date | Assignment due date. |
| `id` | string | Assignment ID. |
| `result` | number | Assignment result percentage. |
| `score` | number | Assignment score. |
| `status` | string | Assignment status. |
| `url` | string | Innform tracking URL. |
| `user` | object | Assigned user summary. |

## Native endpoint

Through the native Innform API, this operation is `GET /assignments` (base URL `https://api.innform.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assignments.md) for the provider-specific parameters and requirements.

