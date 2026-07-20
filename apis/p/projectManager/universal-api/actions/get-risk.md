# ProjectManager: Get Risk

Retrieves a risk from ProjectManager.

```
GET https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/get-risk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/get-risk?connectionId=$CONNECTION_ID&riskId=55555555-5555-5555-5555-555555555555" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "riskId": "55555555-5555-5555-5555-555555555555"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/get-risk?${params}`, {
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
| `riskId` | string | yes | The id of the risk Example: `55555555-5555-5555-5555-555555555555`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignments": {
        "projectId": "string",
        "resourceId": "string",
        "taskId": "string"
      },
      "commentsCount": 1,
      "createDate": "string",
      "discussionData": {
        "count": 1,
        "lastReadDate": "string",
        "lastUpdatedDate": "string"
      },
      "dueDate": "string",
      "fileData": {
        "count": 1,
        "lastReadDate": "string",
        "lastUpdatedDate": "string"
      },
      "filesCount": 1,
      "id": "string",
      "impact": 1,
      "likelihood": 1,
      "modifyDate": "string",
      "name": "Ava Chen",
      "notes": "string",
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
      "percentComplete": 1,
      "priority": 1,
      "project": {
        "id": "string",
        "name": "Ava Chen",
        "shortId": "string"
      },
      "projectId": "string",
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
      "resolution": "string",
      "responseId": 1,
      "riskTypeId": 1,
      "shortId": "string",
      "tags": {
        "color": "string",
        "id": "string",
        "name": "Ava Chen"
      },
      "taskTypeId": 1,
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignments.projectId` | string |  |
| `assignments.resourceId` | string |  |
| `assignments.taskId` | string |  |
| `commentsCount` | number |  |
| `createDate` | string |  |
| `discussionData.count` | number |  |
| `discussionData.lastReadDate` | string |  |
| `discussionData.lastUpdatedDate` | string |  |
| `dueDate` | string |  |
| `fileData.count` | number |  |
| `fileData.lastReadDate` | string |  |
| `fileData.lastUpdatedDate` | string |  |
| `filesCount` | number |  |
| `id` | string |  |
| `impact` | number |  |
| `likelihood` | number |  |
| `modifyDate` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `owner.avatarUrl` | string |  |
| `owner.color` | string |  |
| `owner.email` | string |  |
| `owner.firstName` | string |  |
| `owner.id` | string |  |
| `owner.initials` | string |  |
| `owner.isActive` | boolean |  |
| `owner.lastName` | string |  |
| `percentComplete` | number |  |
| `priority` | number |  |
| `project.id` | string |  |
| `project.name` | string |  |
| `project.shortId` | string |  |
| `projectId` | string |  |
| `recurring` | boolean |  |
| `recurringParentTaskId` | string |  |
| `recurringSettings.endsAfter` | number |  |
| `recurringSettings.endsOn` | string |  |
| `recurringSettings.repeatEvery` | number |  |
| `recurringSettings.repeatOn` | array<number> |  |
| `recurringSettings.repeatOn2Level` | number |  |
| `recurringSettings.type` | number |  |
| `resolution` | string |  |
| `responseId` | number |  |
| `riskTypeId` | number |  |
| `shortId` | string |  |
| `tags.color` | string |  |
| `tags.id` | string |  |
| `tags.name` | string |  |
| `taskTypeId` | number |  |
| `version` | number |  |

## Native endpoint

Through the native ProjectManager API, this operation is `GET /api/data/risks/:riskId` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-risk.md) for the provider-specific parameters and requirements.

