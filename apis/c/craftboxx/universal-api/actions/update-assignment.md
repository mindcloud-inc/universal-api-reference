# Craftboxx: Update Assignment

Updates an assignment in Craftboxx.

```
PUT https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/update-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Craftboxx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/update-assignment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assignmentId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/update-assignment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assignmentId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignmentId` | number | yes | The Craftboxx assignment ID. |
| `end` | string | no | The assignment end timestamp. |
| `start` | string | no | The assignment start timestamp. |
| `state` | string | no | The assignment state. |
| `title` | string | no | The assignment title. |

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

Through the native Craftboxx API, this operation is `PUT assignments/:assignmentId` (base URL `https://api.craftboxx.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-assignment.md) for the provider-specific parameters and requirements.

