# Zoho Projects: Get Project Details

Retrieves project details from Zoho Projects.

```
GET https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/get-project-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/get-project-details?connectionId=$CONNECTION_ID&portalId=string&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "portalId": "string",
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/get-project-details?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "budgetInfo": {
        "trackingMethod": "string"
      },
      "businessHoursId": "string",
      "createdBy": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "fullName": "Ava Chen",
        "lastName": "Chen",
        "name": "Ava Chen",
        "zpuid": "string",
        "zuid": 1
      },
      "createdTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isCompleted": true,
      "isPublicProject": true,
      "isRollupProject": true,
      "isStrictProject": true,
      "issues": {
        "closedCount": 1,
        "openCount": 1
      },
      "key": "string",
      "layout": {
        "id": "string",
        "isDefault": true,
        "name": "Ava Chen",
        "type": "string"
      },
      "milestones": {
        "closedCount": 1,
        "openCount": 1
      },
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "owner": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "fullName": "Ava Chen",
        "lastName": "Chen",
        "name": "Ava Chen",
        "zpuid": "string",
        "zuid": 1
      },
      "percentComplete": 1,
      "projectGroup": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "projectType": "string",
      "status": {
        "color": "string",
        "colorHexcode": "string",
        "id": "string",
        "isClosedType": true,
        "name": "Ava Chen"
      },
      "tasks": {
        "closedCount": 1,
        "openCount": 1
      },
      "updatedBy": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "fullName": "Ava Chen",
        "lastName": "Chen",
        "name": "Ava Chen",
        "zpuid": "string",
        "zuid": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `budgetInfo.trackingMethod` | string |  |
| `businessHoursId` | string |  |
| `createdBy.email` | string |  |
| `createdBy.firstName` | string |  |
| `createdBy.fullName` | string |  |
| `createdBy.lastName` | string |  |
| `createdBy.name` | string |  |
| `createdBy.zpuid` | string |  |
| `createdBy.zuid` | number |  |
| `createdTime` | date |  |
| `id` | string |  |
| `isCompleted` | boolean |  |
| `isPublicProject` | boolean |  |
| `isRollupProject` | boolean |  |
| `isStrictProject` | boolean |  |
| `issues.closedCount` | number |  |
| `issues.openCount` | number |  |
| `key` | string |  |
| `layout.id` | string |  |
| `layout.isDefault` | boolean |  |
| `layout.name` | string |  |
| `layout.type` | string |  |
| `milestones.closedCount` | number |  |
| `milestones.openCount` | number |  |
| `modifiedTime` | date |  |
| `name` | string |  |
| `owner.email` | string |  |
| `owner.firstName` | string |  |
| `owner.fullName` | string |  |
| `owner.lastName` | string |  |
| `owner.name` | string |  |
| `owner.zpuid` | string |  |
| `owner.zuid` | number |  |
| `percentComplete` | number |  |
| `projectGroup.id` | string |  |
| `projectGroup.name` | string |  |
| `projectGroup.type` | string |  |
| `projectType` | string |  |
| `status.color` | string |  |
| `status.colorHexcode` | string |  |
| `status.id` | string |  |
| `status.isClosedType` | boolean |  |
| `status.name` | string |  |
| `tasks.closedCount` | number |  |
| `tasks.openCount` | number |  |
| `updatedBy.email` | string |  |
| `updatedBy.firstName` | string |  |
| `updatedBy.fullName` | string |  |
| `updatedBy.lastName` | string |  |
| `updatedBy.name` | string |  |
| `updatedBy.zpuid` | string |  |
| `updatedBy.zuid` | number |  |

## Native endpoint

Through the native Zoho Projects API, this operation is `GET /portal/[:PORTALID]/projects/[:PROJECTID]` (base URL `https://projectsapi.zoho.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-details.md) for the provider-specific parameters and requirements.

