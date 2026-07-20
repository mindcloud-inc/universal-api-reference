# Podio: List Tasks

Retrieves a list of tasks from Podio.

```
GET https://connect.mindcloud.co/v1/universal/podio/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podio/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podio/latest/actions/list-tasks?${params}`, {
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
| `app[]` | array<number> | no | App ids to filter by. Example: `12345`. |
| `completed` | boolean | no | True to get completed tasks, false to get active tasks. |
| `dueDate` | string | no | Date or date range for the due date. Example: `2026-03-01-2026-03-31`. |
| `grouping` | list<string> | no | Field to group tasks by. One of: `app`, `created_by`, `due_date`, `org`, `responsible`, `space`. |
| `label` | number | no | Label id to match. Example: `12345`. |
| `reference` | string | no | Task reference in the form type:id. Example: `item:12345;status:67890`. |
| `responsible` | number | no | Auth objects or user ids assigned to the task. Example: `77147060`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `completedBy` | string | no | Auth objects for who completed the task. |
| `completedOn` | string | no | Date or date range for when the task was completed. Example: `2026-03-01-2026-03-31`. |
| `createdBy` | string | no | Auth objects for who created the task. |
| `createdOn` | string | no | Date or date range for when the task was created. Example: `2026-03-01-2026-03-31`. |
| `createdVia` | number | no | App id the task was created through. Example: `12345`. |
| `externalId` | string | no | External id of the associated app item. Example: `external-item-001`. |
| `files` | boolean | no | True to get tasks with files, false otherwise. |
| `org[]` | array<number> | no | Organization ids to filter by. Example: `12345`. |
| `reassigned` | boolean | no | True to get reassigned tasks, false otherwise. |
| `space[]` | array<number> | no | Space ids to filter by. Example: `12345`. |
| `view` | list | no | One of: `full`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": [
        {}
      ],
      "completedBy": {},
      "completedOn": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "createdOn": "2026-05-07T12:00:00.000Z",
      "createdVia": {},
      "description": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "externalId": "string",
      "files": [
        {}
      ],
      "link": "https://example.com",
      "responsible": {},
      "rights": [
        "string"
      ],
      "spaceId": 1,
      "status": "string",
      "taskId": 1,
      "text": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments` | array<object> |  |
| `completedBy` | object |  |
| `completedOn` | date |  |
| `createdBy` | object |  |
| `createdOn` | date |  |
| `createdVia` | object |  |
| `description` | string |  |
| `dueDate` | date |  |
| `externalId` | string |  |
| `files` | array<object> |  |
| `link` | string |  |
| `responsible` | object |  |
| `rights` | array<string> |  |
| `spaceId` | number |  |
| `status` | string |  |
| `taskId` | number |  |
| `text` | string |  |

## Native endpoint

Through the native Podio API, this operation is `GET /task/` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

