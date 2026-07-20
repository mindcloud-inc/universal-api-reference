# ProjectManager: Update Meeting

Updates an existing meeting in ProjectManager.

```
PUT https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/update-meeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/update-meeting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "meetingId": "44444444-4444-4444-4444-444444444444"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/update-meeting', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "meetingId": "44444444-4444-4444-4444-444444444444"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `meetingId` | string | yes | the id of the meeting Example: `44444444-4444-4444-4444-444444444444`. |
| `name` | string | no | The common name of this Task. Example: `MindCloud Sample`. |
| `description` | string | no | This field contains the task's "Note" or "Description", which is a description of the work to be done to complete the task. Within the ProjectManager application, you can use this field as follows: * When in the Board or List view, click on a task to open the task panel, then edit the "Description" field. Example: `MindCloud sample description.`. |
| `priorityId` | number | no | Return the priority of a task Example: `88888888-8888-8888-8888-888888888888`. |
| `plannedStartDate` | string | no | The date when work on this Task is planned to begin. This value contains only the date in year-month-day format. For display, this date will always be shown as this same year-month-day regardless of time zone. Example: `2026-04-10`. |
| `durationMinutes` | number | no | The duration (in 15-minute increments) for this Meeting. Example: `1`. |
| `assignees[]` | array<string> | no | If specified, replaces the list of resources assigned to this meeting. Example: `sample`. |
| `assignees[]` | array<string> | no | If specified, replaces the list of resources assigned to this meeting. Example: `sample`. |
| `assignees[]` | array<string> | no | If specified, replaces the list of resources assigned to this meeting. Example: `sample`. |
| `recurring` | boolean | no | Indicates whether this task participates in a recurring series. true if the task is part of a recurrence (series parent when is, or a child otherwise); false if it is a standalone task. When saved as false during an update, the service layer detaches the task from its series, which clears parent/child relationships including and recurringSettings. Example: `true`. |

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

Through the native ProjectManager API, this operation is `PUT /api/data/meetings/:meetingId` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-meeting.md) for the provider-specific parameters and requirements.

