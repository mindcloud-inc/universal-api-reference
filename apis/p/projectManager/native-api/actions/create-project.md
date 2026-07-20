# Create Project with ProjectManager

Creates a new project in ProjectManager.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/data/projects`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Create Project](https://developer.projectmanager.com/api-reference/project/create-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | The name of the Project. |
| `description` | body | `string` | no | An optional description of the Project |
| `shortId` | body | `string` | no | Specify the shortId for this project. If left blank a shortId will be generated.              A short identifier that uniquely identifies this Project within your Workspace using a single letter followed by a number.  This code can be used for APIs that accept Project unique identifiers.              You can observe the short ID within the application by observing the URL of the page you visit when you click on this project.  The page's URL will appear in the form `https://pm.app.projectmanager.com/project/board/D16` - in this example, the `ShortId` is `D16`.              This id can only be set on creation, and can not be updated. |
| `shortName` | body | `string` | no | An optional project short name. Up to 7 symbols |
| `folderId` | body | `string` | no | The unique identifier of the folder of this project, or null if not assigned. |
| `projectAccess` | body | `object` | no | Project Access object |
| `projectAccess.everyone` | body | `boolean` | no | If set to true every user will get access to this project |
| `projectAccess.members[]` | body | `array<object>` | no | If everyone is set to false the list of members will be used to give people access |
| `projectAccess.members[]` | body | `array<object>` | no | If everyone is set to false the list of members will be used to give people access |
| `projectAccess.members[]` | body | `array<object>` | no | If everyone is set to false the list of members will be used to give people access |
| `customerId` | body | `string` | no | The unique identifier of the customer for this project, or null if not customer specific |
| `managerId` | body | `string` | no | The unique identifier of the manager of this project, or null if not assigned. |
| `chargeCodeId` | body | `string` | no | The unique identifier of the ChargeCode for this Project, if one has been selected. |
| `statusId` | body | `string` | no | The ProjectStatus chosen for this Project, if one has been selected. |
| `priorityId` | body | `string` | no | The ProjectPriority level of this Project, if one has been selected. |
| `hourlyRate` | body | `number` | no | The default hourly rate for work on this Project.  This rate will be used if an assignee working on this Project does not have an hourly rate configured in their profile. |
| `budget` | body | `number` | no | The proposed budget for this Project. |
| `statusUpdate` | body | `string` | no | Contains an optional status update for Projects that can be used to summarize the status of multiple Projects at a glance.              You can edit the StatusUpdate field on the Portfolio page of the application. |
| `templateId` | body | `string` | no | When creating a Project, you can optionally specify a Template to use to construct the Project using a collection of pre-designed Tasks.              Specifying a value in the TemplateId field will copy default settings for Tasks from your template Project into the newly created Project.              This field does not support custom templates.  You must choose from a list of ProjectManager-supplied templates. |
| `template` | body | `boolean` | no | True if this Project is a Template project. Template projects can be used as |
| `targetDate` | body | `string` | no | The target planned completion date for this Project, or null if one has not been selected.  This value can be updated in the Project Settings page or the Portfolio Project page within the application. |
| `favorite` | body | `boolean` | no | True if this Project is marked as favorite for current user |
| `updatePlannedWithActual` | body | `boolean` | no | True if allow actual dates to update planned dates |
| `taskStatusCreate[]` | body | `array<object>` | no | Create default task status upfront |
| `taskStatusCreate[]` | body | `array<object>` | no | Create default task status upfront |
| `taskStatusCreate[]` | body | `array<object>` | no | Create default task status upfront |
| `workingDays` | body | `object` | no | Working Days object |
| `workingDays.monday` | body | `boolean` | no | Set this value to true if Monday is considered a working day for this project. |
| `workingDays.tuesday` | body | `boolean` | no | Set this value to true if Tuesday is considered a working day for this project. |
| `workingDays.wednesday` | body | `boolean` | no | Set this value to true if Wednesday is considered a working day for this project. |
| `workingDays.thursday` | body | `boolean` | no | Set this value to true if Thursday is considered a working day for this project. |
| `workingDays.friday` | body | `boolean` | no | Set this value to true if Friday is considered a working day for this project. |
| `workingDays.saturday` | body | `boolean` | no | Set this value to true if Saturday is considered a working day for this project. |
| `workingDays.sunday` | body | `boolean` | no | Set this value to true if Sunday is considered a working day for this project. |
| `externalReferenceId` | body | `string` | no | An optional external reference identifier for this Project. This value can be used to link the Project to records in external systems, such as ERP, CRM, or other integrations. |
| `weekStartsOnMonday` | body | `boolean` | no | Controls which day is considered the first day of the week for this project. If not specified, this will be Sunday in the US and Monday everywhere else. If true, the week starts on Monday. If false, the week starts on Sunday. |
