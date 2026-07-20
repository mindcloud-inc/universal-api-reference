# ProjectManager: Retrieve Notifications

Retrieves notifications from ProjectManager.

```
GET https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-notifications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/retrieve-notifications?${params}`, {
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
| `lastId` | string | no | To continue loading more notifications in a series of requests, provide the ID of the oldest notification from the currently loaded batch as the `lastId` parameter Example: `88888888-8888-8888-8888-888888888888`. |
| `senderId` | string | no | Filter the notifications to only those sent by the user with the specified ID Example: `88888888-8888-8888-8888-888888888888`. |
| `notificationTypes[]` | array<string> | no | Specifies the types of notifications to return. If not provided, all notifications will be returned. Example: `sample`. |
| `asFlatList` | boolean | no | If set to true all notifications will be returned as a flat list, otherwise they will be grouped by parent in the same manner as displayed in the UI. Example: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": {
        "children": [
          {}
        ],
        "createDate": "string",
        "data": {
          "assigneeId": "string",
          "fileName": "Ava Chen",
          "projectId": "string",
          "projectName": "Ava Chen",
          "projectShortId": "string",
          "senderFirstName": "Ava",
          "shareId": "string",
          "taskId": "string",
          "taskName": "Ava Chen",
          "taskShortId": "string",
          "view": "string"
        },
        "id": "string",
        "message": "string",
        "notificationType": "string",
        "readDate": "string",
        "senderId": "string",
        "subject": "string"
      },
      "totalCount": 1,
      "unreadCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items.children` | array<object> |  |
| `items.createDate` | string |  |
| `items.data.assigneeId` | string |  |
| `items.data.fileName` | string |  |
| `items.data.projectId` | string |  |
| `items.data.projectName` | string |  |
| `items.data.projectShortId` | string |  |
| `items.data.senderFirstName` | string |  |
| `items.data.shareId` | string |  |
| `items.data.taskId` | string |  |
| `items.data.taskName` | string |  |
| `items.data.taskShortId` | string |  |
| `items.data.view` | string |  |
| `items.id` | string |  |
| `items.message` | string |  |
| `items.notificationType` | string |  |
| `items.readDate` | string |  |
| `items.senderId` | string |  |
| `items.subject` | string |  |
| `totalCount` | number |  |
| `unreadCount` | number |  |

## Native endpoint

Through the native ProjectManager API, this operation is `GET /api/data/notifications` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-notifications.md) for the provider-specific parameters and requirements.

