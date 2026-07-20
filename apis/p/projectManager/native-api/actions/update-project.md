# Update Project with ProjectManager

Updates an existing project in ProjectManager.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/data/projects/:projectId`
- **Base URL:** `https://api.projectmanager.com`
- **Official documentation:** [Update Project](https://developer.projectmanager.com/api-reference/project/update-project)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The unique identifier of the Project to update |
| `name` | body | `string` | no | The name of the Project. |
| `shortName` | body | `string` | no | The short name of the Project. |
| `description` | body | `string` | no | An optional description of the Project |
| `targetDate` | body | `string` | no | The target planned completion date for this Project, or null if one has not been selected.  This value can be updated in the Project Settings page or the Portfolio Project page within the application. |
| `folderId` | body | `string` | no | To move this Project into a ProjectFolder, set this to the unique identifier of the ProjectFolder. |
| `customerId` | body | `string` | no | To assign this Project to a ProjectCustomer, set this to the unique identifier of the ProjectCustomer.              If set to an empty guid the Project will be unassigned from the current ProjectCustomer. |
| `managerId` | body | `string` | no | To assign this Project to a ProjectManager, set this to the unique identifier of the ProjectManager. |
| `chargeCodeId` | body | `string` | no | To set the ChargeCode for this Project, set this to the unique identifier of the ChargeCode to use for this Project. |
| `statusId` | body | `string` | no | To change the ProjectStatus of this Project, set this to the unique identifier of the ProjectStatus. |
| `priorityId` | body | `string` | no | To change the ProjectPriority of this Project, set this to the unique identifier of the ProjectPriority. |
| `hourlyRate` | body | `number` | no | To change the hourly rate of this Project, set this to the new amount. |
| `budget` | body | `number` | no | To change the budget of this Project, set this to the new amount. |
| `statusUpdate` | body | `string` | no | To update the Project's status text, set this to the new status text. |
| `favorite` | body | `boolean` | no | Mark this project as favorite for the logged in user. |
| `template` | body | `boolean` | no | True if this Project is a template that will be reused as a framework for future Projects.              You can save a Project as a template and reuse it in the future for creating additional Projects.  If this Project is a template, set this to `true` and this template will be available to choose from when creating a new Project within the application. |
| `updatePlannedWithActual` | body | `boolean` | no | True if allow actual dates to update planned dates |
| `notes` | body | `string` | no | To update the project notes |
| `externalReferenceId` | body | `string` | no | An optional external reference identifier for this Project. This value can be used to link the Project to records in external systems, such as ERP, CRM, or other integrations. |
