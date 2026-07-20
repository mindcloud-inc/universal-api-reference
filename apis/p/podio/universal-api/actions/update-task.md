# Podio: Update Task

Updates an existing task in Podio.

```
PUT https://connect.mindcloud.co/v1/universal/podio/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/podio/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "12345"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/podio/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "12345"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | The ID of the task to update. Example: `12345`. |
| `text` | string | no | The updated task title text. Example: `Follow up with vendor`. |
| `description` | string | no | The updated task description. Example: `Update the task details`. |
| `dueDate` | date | no | The new due date in the user's timezone. Example: `2026-03-15`. |
| `dueTime` | string | no | The new due time in the user's timezone. Example: `14:30`. |
| `responsible` | string | no | The user ID of the responsible user. Example: `123456`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `private` | boolean | no | Whether the task should be private. |
| `refType` | string | no | The reference type for the task. Example: `item`. |
| `refId` | string | no | The reference ID for the task. Example: `987654`. |
| `completed` | boolean | no | Mark the task as completed or not completed. |
| `labels[]` | array<string> | no | A list of label IDs or label texts for the task. |
| `fileIds[]` | array<string> | no | A list of uploaded file IDs to attach to the task. |
| `reminder` | object | no | Optional reminder settings for the task. |
| `reminder.remindDelta` | number | no | Minutes before the due date to trigger the reminder. Leave empty to clear the existing reminder. Example: `30`. |
| `hook` | boolean | no | Run Podio hooks for the change. |
| `silent` | boolean | no | Suppress stream bumping and notifications for the update. |

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
      "completedVia": {},
      "createdBy": {},
      "createdOn": "2026-05-07T12:00:00.000Z",
      "createdVia": {},
      "description": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "dueOn": "2026-05-07T12:00:00.000Z",
      "dueTime": "string",
      "externalId": "string",
      "files": [
        {}
      ],
      "group": "string",
      "labels": [
        {}
      ],
      "link": "https://example.com",
      "presence": {},
      "private": true,
      "push": {},
      "recurrence": {},
      "ref": {},
      "reminder": {},
      "responsible": {},
      "rights": [
        "string"
      ],
      "spaceId": 1,
      "started": true,
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
| `completedVia` | object |  |
| `createdBy` | object |  |
| `createdOn` | date |  |
| `createdVia` | object |  |
| `description` | string |  |
| `dueDate` | date |  |
| `dueOn` | date |  |
| `dueTime` | string |  |
| `externalId` | string |  |
| `files` | array<object> |  |
| `group` | string |  |
| `labels` | array<object> |  |
| `link` | string |  |
| `presence` | object |  |
| `private` | boolean |  |
| `push` | object |  |
| `recurrence` | object |  |
| `ref` | object |  |
| `reminder` | object |  |
| `responsible` | object |  |
| `rights` | array<string> |  |
| `spaceId` | number |  |
| `started` | boolean |  |
| `status` | string |  |
| `taskId` | number |  |
| `text` | string |  |

## Native endpoint

Through the native Podio API, this operation is `PUT /task/:task_id` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

