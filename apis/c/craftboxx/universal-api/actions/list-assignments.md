# Craftboxx: List Assignments

Returns assignments from Craftboxx.

```
GET https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/list-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Craftboxx `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/list-assignments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/list-assignments?${params}`, {
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
| `q` | string | no | Search assignments by a broad Craftboxx query string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "end": "2026-05-07T12:00:00.000Z",
      "first_line": "string",
      "id": 1,
      "interfaces": [
        "string"
      ],
      "planner_changelog_url": "https://example.com",
      "planner_delete_url": "https://example.com",
      "planner_details_url": "https://example.com",
      "planner_edit_url": "https://example.com",
      "project_id": 1,
      "second_line": "string",
      "start": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "timezone": "string",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Creation timestamp. |
| `duration` | number | Assignment duration in minutes. |
| `end` | date | End timestamp. |
| `first_line` | string | Primary display line. |
| `id` | number | Assignment ID. |
| `interfaces` | array<string> | Available interface flags. |
| `planner_changelog_url` | string | Planner changelog URL. |
| `planner_delete_url` | string | Planner delete URL. |
| `planner_details_url` | string | Planner details URL. |
| `planner_edit_url` | string | Planner edit URL. |
| `project_id` | number | Project ID. |
| `second_line` | string | Secondary display line. |
| `start` | date | Start timestamp. |
| `state` | string | Assignment state. |
| `timezone` | string | Assignment timezone. |
| `title` | string | Assignment title. |
| `updated_at` | date | Update timestamp. |

## Native endpoint

Through the native Craftboxx API, this operation is `GET assignments` (base URL `https://api.craftboxx.de`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-assignments.md) for the provider-specific parameters and requirements.

