# Podio: Create Task

Creates a new task in Podio.

```
POST https://connect.mindcloud.co/v1/universal/podio/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/podio/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "Follow up with the client"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/podio/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "Follow up with the client"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | yes | Text of the task. Example: `Follow up with the client`. |
| `description` | string | no | Description of the task. Example: `Add context for the task`. |
| `dueDate` | date | no | Due date in YYYY-MM-DD format. Example: `2026-03-15`. |
| `dueTime` | string | no | Time of the due date in HH:MM format. Example: `14:30`. |
| `dueOn` | string | no | Example: `2026-03-15 14:30:00`. |
| `responsible[]` | array<number> | no | User id, auth object, or list of user ids to assign. Example: `77147060`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `refType` | string | no | Example: `item`. |
| `private` | boolean | no | True to make the task private. |
| `refId` | number | no | Example: `12345`. |
| `hook` | boolean | no |  |
| `silent` | boolean | no |  |
| `externalId` | string | no | Example: `external-task-001`. |
| `fileIds[]` | array<number> | no | Example: `12345`. |
| `labels[]` | array<string> | no | Example: `Tutorials`. |
| `labelIds[]` | array<number> | no | Example: `5754406`. |
| `reminder` | object | no |  |
| `recurrence` | object | no |  |

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

Through the native Podio API, this operation is `POST /task/` (base URL `https://api.podio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

