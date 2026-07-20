# Locu: List Tasks

Retrieves a paginated list of tasks from Locu.

```
GET https://connect.mindcloud.co/v1/universal/locu/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Locu `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/locu/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/locu/latest/actions/list-tasks?${params}`, {
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
| `done` | string | no | Filter tasks by completion flag One of: `0`, `1`. |
| `section` | string | no | Filter tasks by section One of: `0`, `1`, `2`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | no | Filter tasks by project ID |
| `parentId` | string | no | Filter tasks by parent task ID |
| `doneAfter` | date | no | Filter tasks completed after this timestamp |
| `doneBefore` | date | no | Filter tasks completed before this timestamp |
| `includeHtml` | boolean | no | Include description content as HTML |
| `includeMarkdown` | boolean | no | Include description content as Markdown |
| `includePlainText` | boolean | no | Include description content as plain text |
| `includeJson` | boolean | no | Include description content as structured JSON |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "hasMore": true,
      "nextCursor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Tasks in the current page |
| `hasMore` | boolean | Whether another page is available |
| `nextCursor` | string | Cursor for the next page |

## Native endpoint

Through the native Locu API, this operation is `GET /tasks` (base URL `https://api.locu.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

