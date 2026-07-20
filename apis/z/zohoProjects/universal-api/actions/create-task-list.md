# Zoho Projects: Create Task List

Creates a new task list in Zoho Projects.

```
POST https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/create-task-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/create-task-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "portalId": "string",
  "projectId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/create-task-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "portalId": "string",
    "projectId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `portalId` | string | yes | Portal identifier from Zoho Projects. |
| `projectId` | string | yes | Project identifier from Zoho Projects. |
| `name` | string | yes | Task list name. |
| `milestone.id` | string | no | Associated milestone identifier. |
| `flag` | string | no | Task list flag. Accepted values: internal, external. |
| `status` | string | no | Task list status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "name": "Ava Chen",
        "zpuid": "string",
        "zuid": 1
      },
      "createdTime": "2026-05-07T12:00:00.000Z",
      "createdVia": "string",
      "flag": "string",
      "id": "string",
      "lastUpdatedTime": "2026-05-07T12:00:00.000Z",
      "metaInfo": {
        "hasComments": true,
        "isCompleted": true,
        "isGeneral": true,
        "isNoneMilestoneTasklist": true,
        "isRolled": true
      },
      "milestone": {
        "id": "string",
        "name": "Ava Chen"
      },
      "name": "Ava Chen",
      "sequence": {
        "milestoneSequence": 1,
        "projectSequence": 1
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy.email` | string |  |
| `createdBy.firstName` | string |  |
| `createdBy.lastName` | string |  |
| `createdBy.name` | string |  |
| `createdBy.zpuid` | string |  |
| `createdBy.zuid` | number |  |
| `createdTime` | date |  |
| `createdVia` | string |  |
| `flag` | string |  |
| `id` | string |  |
| `lastUpdatedTime` | date |  |
| `metaInfo.hasComments` | boolean |  |
| `metaInfo.isCompleted` | boolean |  |
| `metaInfo.isGeneral` | boolean |  |
| `metaInfo.isNoneMilestoneTasklist` | boolean |  |
| `metaInfo.isRolled` | boolean |  |
| `milestone.id` | string |  |
| `milestone.name` | string |  |
| `name` | string |  |
| `sequence.milestoneSequence` | number |  |
| `sequence.projectSequence` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Projects API, this operation is `POST /portal/[:PORTALID]/projects/[:PROJECTID]/tasklists` (base URL `https://projectsapi.zoho.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task-list.md) for the provider-specific parameters and requirements.

