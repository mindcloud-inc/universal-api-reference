# Insightly: Search Tasks

Finds tasks in Insightly by search filters.

```
GET https://connect.mindcloud.co/v1/universal/insightly/latest/actions/search-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Insightly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightly/latest/actions/search-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightly/latest/actions/search-tasks?${params}`, {
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
| `fieldName` | string | no | Filter tasks by this field name. |
| `fieldValue` | string | no | Filter tasks by this field value. |
| `updatedAfterUtc` | string | no | Return tasks updated after this UTC timestamp. |
| `brief` | boolean | no | Return only top-level properties for each task. |
| `countTotal` | boolean | no | Return the total-record count in the response headers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedDateUtc": "2026-05-07T12:00:00.000Z",
      "categoryId": 1,
      "completed": true,
      "completedDateUtc": "2026-05-07T12:00:00.000Z",
      "createdUserId": 1,
      "details": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "opportunityId": 1,
      "ownerUserId": 1,
      "ownerVisible": true,
      "parentTaskId": 1,
      "percentComplete": 1,
      "priority": 1,
      "projectId": 1,
      "reminderDateUtc": "2026-05-07T12:00:00.000Z",
      "responsibleUserId": 1,
      "stageId": 1,
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "taskId": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedDateUtc` | date |  |
| `categoryId` | number |  |
| `completed` | boolean |  |
| `completedDateUtc` | date |  |
| `createdUserId` | number |  |
| `details` | string |  |
| `dueDate` | date |  |
| `opportunityId` | number |  |
| `ownerUserId` | number |  |
| `ownerVisible` | boolean |  |
| `parentTaskId` | number |  |
| `percentComplete` | number |  |
| `priority` | number |  |
| `projectId` | number |  |
| `reminderDateUtc` | date |  |
| `responsibleUserId` | number |  |
| `stageId` | number |  |
| `startDate` | date |  |
| `status` | string |  |
| `taskId` | number |  |
| `title` | string |  |

## Native endpoint

Through the native Insightly API, this operation is `GET {{credentials.apiBaseUrl}}Tasks/Search` (base URL `https://api.na1.insightly.com/v3.1/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-tasks.md) for the provider-specific parameters and requirements.

