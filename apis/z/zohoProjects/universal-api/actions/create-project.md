# Zoho Projects: Create Project

Creates a new project in Zoho Projects.

```
POST https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "portalId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "portalId": "string",
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
| `name` | string | yes | Project name. |
| `description` | string | no | Project description. |
| `projectType` | string | no | Project type. Accepted values: active, template. |
| `owner.zpuid` | string | no | ZPUID of the project owner. |
| `isPublicProject` | boolean | no | Whether the project is public. |
| `startDate` | string | no | Project start date in YYYY-MM-DD format. |
| `endDate` | string | no | Project end date in YYYY-MM-DD format. |
| `status.id` | string | no | Project status identifier. |
| `layout.id` | string | no | Project layout identifier. |
| `addedVia` | string | no | Source from which the project is added. Accepted values: web, api. |
| `isRollupProject` | boolean | no | Whether the project is a roll-up project. |
| `copyFrom` | string | no | Template ID or existing project ID to copy from. |

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

Through the native Zoho Projects API, this operation is `POST /portal/[:PORTALID]/projects` (base URL `https://projectsapi.zoho.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

