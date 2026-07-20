# ProjectManager: Create Meeting

Creates a new meeting in ProjectManager.

```
POST https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/create-meeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/create-meeting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/create-meeting', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | The common name of this Task. Example: `MindCloud Sample`. |
| `description` | string | no | This field contains the task's "Note" or "Description", which is a description of the work to be done to complete the task. Within the ProjectManager application, you can use this field as follows: * When in the Board or List view, click on a task to open the task panel, then edit the "Description" field. Example: `MindCloud sample description.`. |
| `startDate` | string | no | The date when work on this Task is planned to begin. This value contains only the date in year-month-day format. For display, this date will always be shown as this same year-month-day regardless of time zone. time needs to be in 15-minute increments, valid values are 0, 15, 30, 45 Example: `2026-04-10T09:00:00Z`. |
| `durationMinutes` | number | no | The duration (in 15-minute increments) for this Meeting. Example: `1`. |
| `assignees[]` | array<string> | no | Specify a list of resources to assign to this NPT Example: `sample`. |
| `assignees[]` | array<string> | no | Specify a list of resources to assign to this NPT Example: `sample`. |
| `assignees[]` | array<string> | no | Specify a list of resources to assign to this NPT Example: `sample`. |
| `priority` | number | no | The numeric of the Priority for this Meeting Example: `1`. |
| `projectId` | string | no | The unique identifier of the Project for this Meeting Example: `11111111-1111-1111-1111-111111111111`. |

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

Through the native ProjectManager API, this operation is `POST /api/data/meetings` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-meeting.md) for the provider-specific parameters and requirements.

