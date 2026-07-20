# ProjectManager: Update Risk

Updates an existing risk in ProjectManager.

```
PUT https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/update-risk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/update-risk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "riskId": "55555555-5555-5555-5555-555555555555"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/update-risk', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "riskId": "55555555-5555-5555-5555-555555555555"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `riskId` | string | yes | The id of the risk Example: `55555555-5555-5555-5555-555555555555`. |
| `name` | string | no | The common name of this Risk. Example: `MindCloud Sample`. |
| `dueDate` | string | no | The date when this risk is expected to be resolved. Example: `2026-04-15`. |
| `percentComplete` | string | no | Percentage completion (0–100). Example: `sample-percentcomplete`. |
| `priority` | string | no | Priority of the risk. Example: `sample-priority`. |
| `impact` | string | no | The potential effect of the risk. Example: `sample-impact`. |
| `likelihood` | string | no | Probability of the risk occurring. Example: `sample-likelihood`. |
| `responseId` | string | no | Planned or implemented response. Avoid it, Mitigate, Transfer, Accept Example: `88888888-8888-8888-8888-888888888888`. |
| `resolution` | string | no | Actions taken or planned to address the risk. Example: `sample-resolution`. |
| `description` | string | no | Additional comments or observations. Example: `MindCloud sample description.`. |
| `assignees` | string | no | Users assigned to the risk. Replaces existing assignments when provided. Example: `sample-assignees`. |
| `tagIds` | string | no | Tags applied to the risk. Replaces existing tags when provided. Example: `sample-tagids`. |
| `riskTypeId` | string | no | The type of risk. Risk = 1 Assumption = 2 Issue = 3 Dependency = 4 Change = 5 Example: `88888888-8888-8888-8888-888888888888`. |

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
      "dueDate": "string",
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
| `dueDate` | string |  |
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

Through the native ProjectManager API, this operation is `PUT /api/data/risks/:riskId` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-risk.md) for the provider-specific parameters and requirements.

