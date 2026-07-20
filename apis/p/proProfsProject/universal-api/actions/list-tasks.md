# ProProfs Project: List Tasks

Retrieves a list of tasks from ProProfs Project.

```
GET https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProProfs Project `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/proProfsProject/latest/actions/list-tasks?${params}`, {
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
| `limit` | string | no | Maximum number of records to return. |
| `offset` | string | no | Start position for fetching records. |
| `projectId` | string | no | Filter tasks by project ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "active": "string",
          "archived": "string",
          "billableHours": 1,
          "billed": 1,
          "color": "string",
          "completed": "string",
          "dateCompleted": "string",
          "dateCreated": "string",
          "dateModified": "string",
          "description": "string",
          "dueDate": "string",
          "estimatedCost": "string",
          "estimatedHours": "string",
          "fixedPrice": "string",
          "hourlyRate": "https://example.com",
          "important": "string",
          "notes": "string",
          "notifications": "string",
          "ongoing": "string",
          "price": "string",
          "progress": "string",
          "projectId": "string",
          "projectName": "Ava Chen",
          "recurring": "string",
          "startDate": "string",
          "tags": "string",
          "taskId": "string",
          "taskName": "Ava Chen",
          "taskOrder": "string",
          "trackedSeconds": "string",
          "userId": "string",
          "users": [
            {
              "userId": "string",
              "userName": "Ava Chen"
            }
          ]
        }
      ],
      "paging": {
        "limit": 1,
        "offset": 1,
        "totalRecords": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].active` | string |  |
| `data[].archived` | string |  |
| `data[].billableHours` | number |  |
| `data[].billed` | number |  |
| `data[].color` | string |  |
| `data[].completed` | string |  |
| `data[].dateCompleted` | string |  |
| `data[].dateCreated` | string |  |
| `data[].dateModified` | string |  |
| `data[].description` | string |  |
| `data[].dueDate` | string |  |
| `data[].estimatedCost` | string |  |
| `data[].estimatedHours` | string |  |
| `data[].fixedPrice` | string |  |
| `data[].hourlyRate` | string |  |
| `data[].important` | string |  |
| `data[].notes` | string |  |
| `data[].notifications` | string |  |
| `data[].ongoing` | string |  |
| `data[].price` | string |  |
| `data[].progress` | string |  |
| `data[].projectId` | string |  |
| `data[].projectName` | string |  |
| `data[].recurring` | string |  |
| `data[].startDate` | string |  |
| `data[].tags` | string |  |
| `data[].taskId` | string |  |
| `data[].taskName` | string |  |
| `data[].taskOrder` | string |  |
| `data[].trackedSeconds` | string |  |
| `data[].userId` | string |  |
| `data[].users[].userId` | string |  |
| `data[].users[].userName` | string |  |
| `paging.limit` | number |  |
| `paging.offset` | number |  |
| `paging.totalRecords` | number |  |

## Native endpoint

Through the native ProProfs Project API, this operation is `GET /tasks` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

