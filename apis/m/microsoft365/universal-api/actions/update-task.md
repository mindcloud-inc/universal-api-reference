# Microsoft 365: Update Task

Updates a task in Microsoft 365.

```
PUT https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/update-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/update-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskListId": "AQMkAD...",
  "taskId": "AQMkAG..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/update-task', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskListId": "AQMkAD...",
    "taskId": "AQMkAG..."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskListId` | string | yes | Example: `AQMkAD...`. |
| `taskId` | string | yes | Example: `AQMkAG...`. |
| `title` | string | no | Example: `MindCloud task verification updated`. |
| `body.content` | string | no | Example: `Updated by the Microsoft 365 app verification run`. |
| `importance` | string | no | Example: `high`. |
| `status` | string | no | Example: `completed`. |

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

Through the native Microsoft 365 API, this operation is `PATCH /v1.0/me/todo/lists/{{taskListId}}/tasks/{{taskId}}` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task.md) for the provider-specific parameters and requirements.

