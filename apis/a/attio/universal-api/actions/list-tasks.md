# Attio: List Tasks

Retrieves tasks from Attio.

```
GET https://connect.mindcloud.co/v1/universal/attio/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Attio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/attio/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/attio/latest/actions/list-tasks?${params}`, {
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
| `linkedObject` | string | no | Filter tasks to those linked to a record from the specified object. Example: `people`. |
| `linkedRecordId` | string | no | Filter tasks to those linked to the specified record ID. Example: `891dcbfc-9141-415d-9b2a-2238a6cc012d`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignee` | string | no | Filter tasks by assignee. Example: `50cf242c-7fa3-4cad-87d0-75b1af71c57b`. |
| `isCompleted` | boolean | no | Filter tasks by whether they are completed. |
| `sort` | list<string> | no | Sort order for the returned tasks. One of: `created_at:asc`, `created_at:desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignees": [
        {}
      ],
      "contentPlaintext": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdByActor": {},
      "deadlineAt": "2026-05-07T12:00:00.000Z",
      "id": {},
      "isCompleted": true,
      "linkedRecords": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignees` | array<object> | Task assignees. |
| `contentPlaintext` | string | Plaintext task content. |
| `createdAt` | date | When the task was created. |
| `createdByActor` | object | Actor that created the task. |
| `deadlineAt` | date | Task deadline timestamp, when set. |
| `id` | object | Task identifier payload containing workspace and task ids. |
| `isCompleted` | boolean | Whether the task is completed. |
| `linkedRecords` | array<object> | Records linked to the task. |

## Native endpoint

Through the native Attio API, this operation is `GET /v2/tasks` (base URL `https://api.attio.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

