# ProjectManager: Create Project

Creates a new project in ProjectManager.

```
POST https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/create-project', {
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
| `name` | string | no | The name of the Project. Example: `MindCloud Sample`. |
| `description` | string | no | An optional description of the Project Example: `MindCloud sample description.`. |
| `shortId` | string | no | Specify the shortId for this project. If left blank a shortId will be generated. A short identifier that uniquely identifies this Project within your Workspace using a single letter followed by a number. This code can be used for APIs that accept Project unique identifiers. You can observe the short ID within the application by observing the URL of the page you visit when you click on this project. The page's URL will appear in the form `https://pm.app.projectmanager.com/project/board/D16` - in this example, the `ShortId` is `D16`. This id can only be set on creation, and can not be updated. Example: `88888888-8888-8888-8888-888888888888`. |
| `shortName` | string | no | An optional project short name. Up to 7 symbols Example: `Create Project Short Name`. |
| `folderId` | string | no | The unique identifier of the folder of this project, or null if not assigned. Example: `88888888-8888-8888-8888-888888888888`. |
| `projectAccess` | object | no | Project Access object Example: `[object Object]`. |
| `projectAccess.everyone` | boolean | no | If set to true every user will get access to this project Example: `true`. |
| `projectAccess.members[]` | array<object> | no | If everyone is set to false the list of members will be used to give people access Example: `sample`. |
| `projectAccess.members[]` | array<object> | no | If everyone is set to false the list of members will be used to give people access Example: `sample`. |
| `projectAccess.members[]` | array<object> | no | If everyone is set to false the list of members will be used to give people access Example: `sample`. |
| `customerId` | string | no | The unique identifier of the customer for this project, or null if not customer specific Example: `88888888-8888-8888-8888-888888888888`. |
| `managerId` | string | no | The unique identifier of the manager of this project, or null if not assigned. Example: `88888888-8888-8888-8888-888888888888`. |
| `chargeCodeId` | string | no | The unique identifier of the ChargeCode for this Project, if one has been selected. Example: `88888888-8888-8888-8888-888888888888`. |
| `statusId` | string | no | The ProjectStatus chosen for this Project, if one has been selected. Example: `88888888-8888-8888-8888-888888888888`. |
| `priorityId` | string | no | The ProjectPriority level of this Project, if one has been selected. Example: `88888888-8888-8888-8888-888888888888`. |
| `hourlyRate` | number | no | The default hourly rate for work on this Project. This rate will be used if an assignee working on this Project does not have an hourly rate configured in their profile. Example: `1`. |
| `budget` | number | no | The proposed budget for this Project. Example: `1`. |
| `statusUpdate` | string | no | Contains an optional status update for Projects that can be used to summarize the status of multiple Projects at a glance. You can edit the StatusUpdate field on the Portfolio page of the application. Example: `2026-04-10`. |
| `templateId` | string | no | When creating a Project, you can optionally specify a Template to use to construct the Project using a collection of pre-designed Tasks. Specifying a value in the TemplateId field will copy default settings for Tasks from your template Project into the newly created Project. This field does not support custom templates. You must choose from a list of ProjectManager-supplied templates. Example: `88888888-8888-8888-8888-888888888888`. |
| `template` | boolean | no | True if this Project is a Template project. Template projects can be used as Example: `true`. |
| `targetDate` | string | no | The target planned completion date for this Project, or null if one has not been selected. This value can be updated in the Project Settings page or the Portfolio Project page within the application. Example: `2026-04-10`. |
| `favorite` | boolean | no | True if this Project is marked as favorite for current user Example: `true`. |
| `updatePlannedWithActual` | boolean | no | True if allow actual dates to update planned dates Example: `true`. |
| `taskStatusCreate[]` | array<object> | no | Create default task status upfront Example: `sample`. |
| `taskStatusCreate[]` | array<object> | no | Create default task status upfront Example: `sample`. |
| `taskStatusCreate[]` | array<object> | no | Create default task status upfront Example: `sample`. |
| `workingDays` | object | no | Working Days object Example: `[object Object]`. |
| `workingDays.monday` | boolean | no | Set this value to true if Monday is considered a working day for this project. Example: `true`. |
| `workingDays.tuesday` | boolean | no | Set this value to true if Tuesday is considered a working day for this project. Example: `true`. |
| `workingDays.wednesday` | boolean | no | Set this value to true if Wednesday is considered a working day for this project. Example: `true`. |
| `workingDays.thursday` | boolean | no | Set this value to true if Thursday is considered a working day for this project. Example: `true`. |
| `workingDays.friday` | boolean | no | Set this value to true if Friday is considered a working day for this project. Example: `true`. |
| `workingDays.saturday` | boolean | no | Set this value to true if Saturday is considered a working day for this project. Example: `true`. |
| `workingDays.sunday` | boolean | no | Set this value to true if Sunday is considered a working day for this project. Example: `true`. |
| `externalReferenceId` | string | no | An optional external reference identifier for this Project. This value can be used to link the Project to records in external systems, such as ERP, CRM, or other integrations. Example: `88888888-8888-8888-8888-888888888888`. |
| `weekStartsOnMonday` | boolean | no | Controls which day is considered the first day of the week for this project. If not specified, this will be Sunday in the US and Monday everywhere else. If true, the week starts on Monday. If false, the week starts on Sunday. Example: `true`. |

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

Through the native ProjectManager API, this operation is `POST /api/data/projects` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

