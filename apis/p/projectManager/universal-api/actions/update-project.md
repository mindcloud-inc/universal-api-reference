# ProjectManager: Update Project

Updates an existing project in ProjectManager.

```
PUT https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "11111111-1111-1111-1111-111111111111"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "11111111-1111-1111-1111-111111111111"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The unique identifier of the Project to update Example: `11111111-1111-1111-1111-111111111111`. |
| `name` | string | no | The name of the Project. Example: `MindCloud Sample`. |
| `shortName` | string | no | The short name of the Project. Example: `Update Project Short Name`. |
| `description` | string | no | An optional description of the Project Example: `MindCloud sample description.`. |
| `targetDate` | string | no | The target planned completion date for this Project, or null if one has not been selected. This value can be updated in the Project Settings page or the Portfolio Project page within the application. Example: `2026-04-10`. |
| `folderId` | string | no | To move this Project into a ProjectFolder, set this to the unique identifier of the ProjectFolder. Example: `88888888-8888-8888-8888-888888888888`. |
| `customerId` | string | no | To assign this Project to a ProjectCustomer, set this to the unique identifier of the ProjectCustomer. If set to an empty guid the Project will be unassigned from the current ProjectCustomer. Example: `88888888-8888-8888-8888-888888888888`. |
| `managerId` | string | no | To assign this Project to a ProjectManager, set this to the unique identifier of the ProjectManager. Example: `88888888-8888-8888-8888-888888888888`. |
| `chargeCodeId` | string | no | To set the ChargeCode for this Project, set this to the unique identifier of the ChargeCode to use for this Project. Example: `88888888-8888-8888-8888-888888888888`. |
| `statusId` | string | no | To change the ProjectStatus of this Project, set this to the unique identifier of the ProjectStatus. Example: `88888888-8888-8888-8888-888888888888`. |
| `priorityId` | string | no | To change the ProjectPriority of this Project, set this to the unique identifier of the ProjectPriority. Example: `88888888-8888-8888-8888-888888888888`. |
| `hourlyRate` | number | no | To change the hourly rate of this Project, set this to the new amount. Example: `1`. |
| `budget` | number | no | To change the budget of this Project, set this to the new amount. Example: `1`. |
| `statusUpdate` | string | no | To update the Project's status text, set this to the new status text. Example: `2026-04-10`. |
| `favorite` | boolean | no | Mark this project as favorite for the logged in user. Example: `true`. |
| `template` | boolean | no | True if this Project is a template that will be reused as a framework for future Projects. You can save a Project as a template and reuse it in the future for creating additional Projects. If this Project is a template, set this to `true` and this template will be available to choose from when creating a new Project within the application. Example: `true`. |
| `updatePlannedWithActual` | boolean | no | True if allow actual dates to update planned dates Example: `true`. |
| `notes` | string | no | To update the project notes Example: `MindCloud sample notes.`. |
| `externalReferenceId` | string | no | An optional external reference identifier for this Project. This value can be used to link the Project to records in external systems, such as ERP, CRM, or other integrations. Example: `88888888-8888-8888-8888-888888888888`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {
        "additionalErrors": [
          "string"
        ],
        "message": "string",
        "technicalError": "string"
      },
      "hasError": true,
      "statusCode": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error.additionalErrors` | array<string> |  |
| `error.message` | string |  |
| `error.technicalError` | string |  |
| `hasError` | boolean |  |
| `statusCode` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native ProjectManager API, this operation is `PUT /api/data/projects/:projectId` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

