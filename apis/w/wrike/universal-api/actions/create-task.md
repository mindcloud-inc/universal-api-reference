# Wrike: Create Task

Creates a new task in a Wrike folder.

```
POST https://connect.mindcloud.co/v1/universal/wrike/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrike `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wrike/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "folderId": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wrike/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "folderId": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | yes | Wrike folder ID where the task will be created. |
| `title` | string | yes | Title of task, required |
| `description` | string | no | Description of task, will be left blank if not set |
| `status` | list | no | Task status One of: `Active`, `Cancelled`, `Completed`, `Deferred`. |
| `importance` | list | no | Task importance One of: `High`, `Low`, `Normal`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dates` | string | no | Task dates as a JSON object string |
| `shareds` | string | no | User or invitation IDs as a JSON string array |
| `parents` | string | no | Parent folder IDs as a JSON string array |
| `responsibles` | string | no | Assignee user or invitation IDs as a JSON string array |
| `responsiblePlaceholders` | string | no | Placeholder assignee IDs as a JSON string array |
| `followers` | string | no | Follower user IDs as a JSON string array |
| `follow` | boolean | no | Follow task |
| `priorityBefore` | string | no | Put newly created task before this task ID |
| `priorityAfter` | string | no | Put newly created task after this task ID |
| `superTasks` | string | no | Parent task IDs as a JSON string array |
| `metadata` | string | no | Metadata entries as a JSON string array |
| `customFields` | string | no | Custom field values as a JSON string array |
| `customStatus` | string | no | Custom status ID |
| `effortAllocation` | string | no | Effort allocation as a JSON object string |
| `billingType` | list | no | Task timelog billing type One of: `Billable`, `NonBillable`. |
| `withInvitations` | boolean | no | Include invitations in shared and responsible lists |
| `customItemTypeId` | string | no | Custom item type ID to create a task from |
| `plainTextCustomFields` | boolean | no | Strip HTML tags from custom fields |
| `workScheduleId` | string | no | Work schedule ID to assign to the task |
| `fields` | string | no | Response field names as a JSON string array |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "customStatusId": "string",
      "dates": {},
      "entityTypeId": "string",
      "id": "string",
      "importance": "string",
      "permalink": "https://example.com",
      "priority": "string",
      "scope": "string",
      "status": "string",
      "title": "string",
      "updatedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `createdDate` | date |  |
| `customStatusId` | string |  |
| `dates` | object |  |
| `entityTypeId` | string |  |
| `id` | string |  |
| `importance` | string |  |
| `permalink` | string |  |
| `priority` | string |  |
| `scope` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updatedDate` | date |  |

## Native endpoint

Through the native Wrike API, this operation is `POST /folders/:folderId/tasks` (base URL `https://{{credentials.accessTokenRequest.host}}/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

