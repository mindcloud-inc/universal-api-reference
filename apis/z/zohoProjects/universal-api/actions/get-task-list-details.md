# Zoho Projects: Get Task List Details

Retrieves task list details from Zoho Projects.

```
GET https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/get-task-list-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/get-task-list-details?connectionId=$CONNECTION_ID&portalId=string&projectId=string&tasklistId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "string",
  "projectId": "string",
  "tasklistId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/get-task-list-details?${params}`, {
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
| `portalId` | string | yes | Zoho Projects portal ID. |
| `projectId` | string | yes | Zoho Projects project ID. |
| `tasklistId` | string | yes | Zoho Projects task list ID. |

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

Through the native Zoho Projects API, this operation is `GET /portal/[:PORTALID]/projects/[:PROJECTID]/tasklists/[:TASKLISTID]` (base URL `https://projectsapi.zoho.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-task-list-details.md) for the provider-specific parameters and requirements.

