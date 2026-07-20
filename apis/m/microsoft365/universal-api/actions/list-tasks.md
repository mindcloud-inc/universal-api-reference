# Microsoft 365: List Tasks

Retrieves tasks from a Microsoft 365 task list.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-tasks?connectionId=$CONNECTION_ID&taskListId=AQMkAD..." \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskListId": "AQMkAD..."
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-tasks?${params}`, {
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
| `taskListId` | string | yes | Microsoft To Do task list ID. Example: `AQMkAD...`. |
| `top` | number | no | Default: `10`. Example: `10`. |

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

Through the native Microsoft 365 API, this operation is `GET /v1.0/me/todo/lists/{{taskListId}}/tasks` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tasks.md) for the provider-specific parameters and requirements.

