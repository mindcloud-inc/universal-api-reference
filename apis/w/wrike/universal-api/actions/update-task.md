# Wrike: Update Task

Updates an existing task in Wrike.

```
PUT https://connect.mindcloud.co/v1/universal/wrike/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrike `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wrike/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wrike/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | Wrike task ID. |
| `title` | string | no | Title of task |
| `description` | string | no | Task description |
| `status` | list | no | Task status One of: `Active`, `Cancelled`, `Completed`, `Deferred`. |
| `importance` | list | no | Task importance One of: `High`, `Low`, `Normal`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dates` | string | no | Task dates as a JSON object string |
| `addParents` | string | no | Folder IDs to add as parents, as a JSON string array |
| `removeParents` | string | no | Folder IDs to remove as parents, as a JSON string array |
| `addShareds` | string | no | User or invitation IDs to share with, as a JSON string array |
| `removeShareds` | string | no | User or invitation IDs to unshare, as a JSON string array |
| `addResponsibles` | string | no | User or invitation IDs to add as assignees, as a JSON string array |
| `removeResponsibles` | string | no | User or invitation IDs to remove as assignees, as a JSON string array |
| `addResponsiblePlaceholders` | string | no | Placeholder IDs to add as assignees, as a JSON string array |
| `removeResponsiblePlaceholders` | string | no | Placeholder IDs to remove as assignees, as a JSON string array |
| `addFollowers` | string | no | User IDs to add as followers, as a JSON string array |
| `follow` | boolean | no | Follow task |
| `priorityBefore` | string | no | Put task before this task ID |
| `priorityAfter` | string | no | Put task after this task ID |
| `addSuperTasks` | string | no | Parent task IDs to add, as a JSON string array |
| `removeSuperTasks` | string | no | Parent task IDs to remove, as a JSON string array |
| `metadata` | string | no | Metadata entries to update, as a JSON string array |
| `customFields` | string | no | Custom field values to update, as a JSON string array |
| `customStatus` | string | no | Custom status ID |
| `restore` | boolean | no | Restore task from recycled bin |
| `effortAllocation` | string | no | Effort allocation as a JSON object string |
| `setResponsibleAllocation` | string | no | Responsible allocations as a JSON string array |
| `billingType` | list | no | Task timelog billing type One of: `Billable`, `NonBillable`. |
| `withInvitations` | boolean | no | Include invitations in shared and responsible lists |
| `convertToCustomItemType` | string | no | Custom item type ID |
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

Through the native Wrike API, this operation is `PUT /tasks/:taskId` (base URL `https://{{credentials.accessTokenRequest.host}}/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

