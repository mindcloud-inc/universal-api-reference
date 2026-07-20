# Formitize: List Tasks

Retrieves tasks from Formitize.

```
GET https://connect.mindcloud.co/v1/universal/formitize/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formitize `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formitize/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formitize/latest/actions/list-tasks?${params}`, {
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
| `assignedTo` | string | no | Filter by assigned user ID. |
| `clientId` | string | no | Filter by related client ID. |
| `from` | string | no | Filter tasks with a due date on or after this date. |
| `order` | string | no | Sort direction on due date. |
| `search` | string | no | Search task title and description. |
| `status` | string | no | Filter by task status. |
| `taskType` | string | no | Filter by task type. |
| `to` | string | no | Filter tasks with a due date on or before this date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedTo": 1,
      "createdBy": 1,
      "dateCreated": 1,
      "dateModified": 1,
      "description": "string",
      "dueDate": 1,
      "id": 1,
      "status": 1,
      "tags": [
        "string"
      ],
      "taskType": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedTo` | number |  |
| `createdBy` | number |  |
| `dateCreated` | number |  |
| `dateModified` | number |  |
| `description` | string |  |
| `dueDate` | number |  |
| `id` | number |  |
| `status` | number |  |
| `tags` | array<string> |  |
| `taskType` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Formitize API, this operation is `GET /crm/task/` (base URL `https://service.formitize.com/api/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

