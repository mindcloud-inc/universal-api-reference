# Microsoft 365: Create Task

Creates a new task in Microsoft 365.

```
POST https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskListId": "AQMkAD...",
  "title": "MindCloud task verification"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskListId": "AQMkAD...",
    "title": "MindCloud task verification"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskListId` | string | yes | Example: `AQMkAD...`. |
| `title` | string | yes | Example: `MindCloud task verification`. |
| `body.content` | string | no | Example: `Created by the Microsoft 365 app verification run`. |
| `importance` | string | no | Example: `normal`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": {
        "content": "string",
        "contentType": "string"
      },
      "categories": [
        [
          "string"
        ]
      ],
      "completedDateTime": {
        "dateTime": "string",
        "timeZone": "string"
      },
      "createdDateTime": "string",
      "hasAttachments": true,
      "id": "string",
      "importance": "string",
      "isReminderOn": true,
      "lastModifiedDateTime": "string",
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body.content` | string |  |
| `body.contentType` | string |  |
| `categories[]` | array<string> |  |
| `completedDateTime.dateTime` | string |  |
| `completedDateTime.timeZone` | string |  |
| `createdDateTime` | string |  |
| `hasAttachments` | boolean |  |
| `id` | string |  |
| `importance` | string |  |
| `isReminderOn` | boolean |  |
| `lastModifiedDateTime` | string |  |
| `status` | string |  |
| `title` | string |  |

## Native endpoint

Through the native Microsoft 365 API, this operation is `POST /v1.0/me/todo/lists/{{taskListId}}/tasks` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

