# ProjectManager: Query Projects

Finds projects in ProjectManager.

```
GET https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/query-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/query-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/query-projects?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `top` | number | no | The number of records to return Example: `25`. |
| `skip` | number | no | Skips the given number of records and then returns $top records Example: `0`. |
| `filter` | string | no | Filter the expression according to oData queries Example: `name ne ''`. |
| `orderby` | string | no | Order collection by this field. Example: `createDate desc`. |
| `expand` | string | no | Include related data in the response Example: `tasks`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualFinishDate": "string",
      "actualStartDate": "string",
      "budget": 1,
      "chargeCode": {
        "id": "string",
        "isActive": true,
        "name": "Ava Chen"
      },
      "createDate": "string",
      "creationTemplateId": "string",
      "customer": {
        "id": "string",
        "name": "Ava Chen"
      },
      "description": "string",
      "endDate": "string",
      "externalReferenceId": "string",
      "favorite": true,
      "fieldValues": {
        "createdDate": "string",
        "id": "string",
        "modifiedDate": "string",
        "name": "Ava Chen",
        "shortId": "string",
        "type": "string",
        "value": "string"
      },
      "files": {
        "folder": {
          "id": "string",
          "name": "Ava Chen"
        },
        "id": "string",
        "name": "Ava Chen",
        "task": {
          "id": "string",
          "name": "Ava Chen",
          "shortId": "string"
        },
        "url": "https://example.com"
      },
      "folder": {
        "id": "string",
        "name": "Ava Chen"
      },
      "hourlyRate": 1,
      "id": "string",
      "isTemplate": true,
      "manager": {
        "avatarUrl": "https://example.com",
        "color": "string",
        "id": "string",
        "initials": "string",
        "name": "Ava Chen"
      },
      "members": {
        "avatarUrl": "https://example.com",
        "color": "string",
        "id": "string",
        "initials": "string",
        "name": "Ava Chen",
        "permission": "string",
        "permissionOptions": {
          "collaborate": true,
          "editor": true,
          "guest": true,
          "manager": true,
          "none": true
        },
        "role": "string"
      },
      "modifyDate": "string",
      "name": "Ava Chen",
      "ownerId": "string",
      "percentComplete": 1,
      "plannedFinishDate": "string",
      "plannedStartDate": "string",
      "priority": {
        "id": "string",
        "name": "Ava Chen"
      },
      "shortCode": "string",
      "shortId": "string",
      "startDate": "string",
      "status": {
        "id": "string",
        "isDeleted": true,
        "isSystem": true,
        "name": "Ava Chen"
      },
      "statusUpdate": "string",
      "targetDate": "string",
      "updatePlannedWithActual": true,
      "workingDays": {
        "friday": true,
        "monday": true,
        "saturday": true,
        "sunday": true,
        "thursday": true,
        "tuesday": true,
        "wednesday": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualFinishDate` | string |  |
| `actualStartDate` | string |  |
| `budget` | number |  |
| `chargeCode.id` | string |  |
| `chargeCode.isActive` | boolean |  |
| `chargeCode.name` | string |  |
| `createDate` | string |  |
| `creationTemplateId` | string |  |
| `customer.id` | string |  |
| `customer.name` | string |  |
| `description` | string |  |
| `endDate` | string |  |
| `externalReferenceId` | string |  |
| `favorite` | boolean |  |
| `fieldValues.createdDate` | string |  |
| `fieldValues.id` | string |  |
| `fieldValues.modifiedDate` | string |  |
| `fieldValues.name` | string |  |
| `fieldValues.shortId` | string |  |
| `fieldValues.type` | string |  |
| `fieldValues.value` | string |  |
| `files.folder.id` | string |  |
| `files.folder.name` | string |  |
| `files.id` | string |  |
| `files.name` | string |  |
| `files.task.id` | string |  |
| `files.task.name` | string |  |
| `files.task.shortId` | string |  |
| `files.url` | string |  |
| `folder.id` | string |  |
| `folder.name` | string |  |
| `hourlyRate` | number |  |
| `id` | string |  |
| `isTemplate` | boolean |  |
| `manager.avatarUrl` | string |  |
| `manager.color` | string |  |
| `manager.id` | string |  |
| `manager.initials` | string |  |
| `manager.name` | string |  |
| `members.avatarUrl` | string |  |
| `members.color` | string |  |
| `members.id` | string |  |
| `members.initials` | string |  |
| `members.name` | string |  |
| `members.permission` | string |  |
| `members.permissionOptions.collaborate` | boolean |  |
| `members.permissionOptions.editor` | boolean |  |
| `members.permissionOptions.guest` | boolean |  |
| `members.permissionOptions.manager` | boolean |  |
| `members.permissionOptions.none` | boolean |  |
| `members.role` | string |  |
| `modifyDate` | string |  |
| `name` | string |  |
| `ownerId` | string |  |
| `percentComplete` | number |  |
| `plannedFinishDate` | string |  |
| `plannedStartDate` | string |  |
| `priority.id` | string |  |
| `priority.name` | string |  |
| `shortCode` | string |  |
| `shortId` | string |  |
| `startDate` | string |  |
| `status.id` | string |  |
| `status.isDeleted` | boolean |  |
| `status.isSystem` | boolean |  |
| `status.name` | string |  |
| `statusUpdate` | string |  |
| `targetDate` | string |  |
| `updatePlannedWithActual` | boolean |  |
| `workingDays.friday` | boolean |  |
| `workingDays.monday` | boolean |  |
| `workingDays.saturday` | boolean |  |
| `workingDays.sunday` | boolean |  |
| `workingDays.thursday` | boolean |  |
| `workingDays.tuesday` | boolean |  |
| `workingDays.wednesday` | boolean |  |

## Native endpoint

Through the native ProjectManager API, this operation is `GET /api/data/projects` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-projects.md) for the provider-specific parameters and requirements.

