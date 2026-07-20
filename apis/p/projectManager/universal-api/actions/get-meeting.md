# ProjectManager: Get Meeting

Retrieves a meeting from ProjectManager.

```
GET https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/get-meeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/get-meeting?connectionId=$CONNECTION_ID&meetingId=44444444-4444-4444-4444-444444444444" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "meetingId": "44444444-4444-4444-4444-444444444444"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/get-meeting?${params}`, {
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
| `meetingId` | string | yes | the id of the meeting Example: `44444444-4444-4444-4444-444444444444`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignees": {
        "avatarUrl": "https://example.com",
        "colorName": "Ava Chen",
        "description": "string",
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "initials": "string",
        "isActive": true,
        "lastName": "Chen",
        "name": "Ava Chen",
        "shortName": "Ava Chen"
      },
      "createDate": "string",
      "description": "string",
      "discussionData": {
        "count": 1,
        "lastReadDate": "string",
        "lastUpdatedDate": "string"
      },
      "fileData": {
        "count": 1,
        "lastReadDate": "string",
        "lastUpdatedDate": "string"
      },
      "id": "string",
      "name": "Ava Chen",
      "owner": {
        "avatarUrl": "https://example.com",
        "color": "string",
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "initials": "string",
        "isActive": true,
        "lastName": "Chen"
      },
      "ownerId": "string",
      "plannedDuration": 1,
      "plannedEffort": 1,
      "plannedFinishDate": "string",
      "plannedStartDate": "string",
      "priorityId": 1,
      "project": {
        "id": "string",
        "name": "Ava Chen",
        "shortId": "string"
      },
      "recurring": true,
      "recurringParentTaskId": "string",
      "recurringSettings": {
        "endsAfter": 1,
        "endsOn": "string",
        "repeatEvery": 1,
        "repeatOn": [
          1
        ],
        "repeatOn2Level": 1,
        "type": 1
      },
      "shortId": "string",
      "tags": {
        "color": "string",
        "id": "string",
        "name": "Ava Chen"
      },
      "todos": {
        "complete": true,
        "createDate": "string",
        "id": "string",
        "modifyDate": "string",
        "text": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignees.avatarUrl` | string |  |
| `assignees.colorName` | string |  |
| `assignees.description` | string |  |
| `assignees.email` | string |  |
| `assignees.firstName` | string |  |
| `assignees.id` | string |  |
| `assignees.initials` | string |  |
| `assignees.isActive` | boolean |  |
| `assignees.lastName` | string |  |
| `assignees.name` | string |  |
| `assignees.shortName` | string |  |
| `createDate` | string |  |
| `description` | string |  |
| `discussionData.count` | number |  |
| `discussionData.lastReadDate` | string |  |
| `discussionData.lastUpdatedDate` | string |  |
| `fileData.count` | number |  |
| `fileData.lastReadDate` | string |  |
| `fileData.lastUpdatedDate` | string |  |
| `id` | string |  |
| `name` | string |  |
| `owner.avatarUrl` | string |  |
| `owner.color` | string |  |
| `owner.email` | string |  |
| `owner.firstName` | string |  |
| `owner.id` | string |  |
| `owner.initials` | string |  |
| `owner.isActive` | boolean |  |
| `owner.lastName` | string |  |
| `ownerId` | string |  |
| `plannedDuration` | number |  |
| `plannedEffort` | number |  |
| `plannedFinishDate` | string |  |
| `plannedStartDate` | string |  |
| `priorityId` | number |  |
| `project.id` | string |  |
| `project.name` | string |  |
| `project.shortId` | string |  |
| `recurring` | boolean |  |
| `recurringParentTaskId` | string |  |
| `recurringSettings.endsAfter` | number |  |
| `recurringSettings.endsOn` | string |  |
| `recurringSettings.repeatEvery` | number |  |
| `recurringSettings.repeatOn` | array<number> |  |
| `recurringSettings.repeatOn2Level` | number |  |
| `recurringSettings.type` | number |  |
| `shortId` | string |  |
| `tags.color` | string |  |
| `tags.id` | string |  |
| `tags.name` | string |  |
| `todos.complete` | boolean |  |
| `todos.createDate` | string |  |
| `todos.id` | string |  |
| `todos.modifyDate` | string |  |
| `todos.text` | string |  |

## Native endpoint

Through the native ProjectManager API, this operation is `GET /api/data/meetings/:meetingId` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-meeting.md) for the provider-specific parameters and requirements.

