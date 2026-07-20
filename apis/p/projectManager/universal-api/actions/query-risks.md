# ProjectManager: Query Risks

Finds risks in ProjectManager.

```
GET https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/query-risks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProjectManager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/query-risks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/projectManager/latest/actions/query-risks?${params}`, {
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

Through the native ProjectManager API, this operation is `GET /api/data/risks` (base URL `https://api.projectmanager.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-risks.md) for the provider-specific parameters and requirements.

