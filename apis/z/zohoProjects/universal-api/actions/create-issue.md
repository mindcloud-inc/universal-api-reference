# Zoho Projects: Create Issue

Creates a new issue in Zoho Projects.

```
POST https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/create-issue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Projects `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/create-issue" \
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
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoProjects/latest/actions/create-issue', {
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
| `portalId` | string | yes | Zoho Projects portal ID. |
| `projectId` | string | yes | Zoho Projects project ID. |
| `name` | string | yes | Issue title. |
| `description` | string | no | Issue description. |
| `flag` | string | no | Issue visibility flag. |
| `associatedTeams.id` | string | no | Associated team ID. |
| `assignee.zpuid` | string | no | Assignee ZPUID. |
| `status.id` | string | no | Issue status ID. |
| `dueDate` | string | no | Issue due date. |
| `releaseMilestone.id` | string | no | Release milestone ID. |
| `affectedMilestone.id` | string | no | Affected milestone ID. |
| `severity.id` | string | no | Issue severity ID. |
| `isItReproducible.id` | string | no | Reproducible value ID. |
| `classification.id` | string | no | Issue classification ID. |
| `module.id` | string | no | Issue module ID. |
| `ratePerHour` | number | no | Billing rate per hour. |
| `costRatePerHour` | number | no | Cost rate per hour. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedVia": "string",
      "assignee": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "name": "Ava Chen",
        "zpuid": "string",
        "zuid": 1
      },
      "classification": {
        "id": "string",
        "value": "string"
      },
      "createdBy": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "lastName": "Chen",
        "name": "Ava Chen",
        "zpuid": "string",
        "zuid": 1
      },
      "createdTime": "2026-05-07T12:00:00.000Z",
      "flag": "string",
      "id": "string",
      "isItReproducible": {
        "id": "string",
        "value": "string"
      },
      "lastUpdatedTime": "2026-05-07T12:00:00.000Z",
      "module": {
        "id": "string",
        "value": "string"
      },
      "name": "Ava Chen",
      "prefix": "string",
      "project": {
        "id": "string",
        "name": "Ava Chen"
      },
      "severity": {
        "id": "string",
        "value": "string"
      },
      "status": {
        "color": "string",
        "colorHexcode": "string",
        "id": "string",
        "isClosedType": true,
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedVia` | string |  |
| `assignee.email` | string |  |
| `assignee.firstName` | string |  |
| `assignee.lastName` | string |  |
| `assignee.name` | string |  |
| `assignee.zpuid` | string |  |
| `assignee.zuid` | number |  |
| `classification.id` | string |  |
| `classification.value` | string |  |
| `createdBy.email` | string |  |
| `createdBy.firstName` | string |  |
| `createdBy.lastName` | string |  |
| `createdBy.name` | string |  |
| `createdBy.zpuid` | string |  |
| `createdBy.zuid` | number |  |
| `createdTime` | date |  |
| `flag` | string |  |
| `id` | string |  |
| `isItReproducible.id` | string |  |
| `isItReproducible.value` | string |  |
| `lastUpdatedTime` | date |  |
| `module.id` | string |  |
| `module.value` | string |  |
| `name` | string |  |
| `prefix` | string |  |
| `project.id` | string |  |
| `project.name` | string |  |
| `severity.id` | string |  |
| `severity.value` | string |  |
| `status.color` | string |  |
| `status.colorHexcode` | string |  |
| `status.id` | string |  |
| `status.isClosedType` | boolean |  |
| `status.name` | string |  |

## Native endpoint

Through the native Zoho Projects API, this operation is `POST /portal/[:PORTALID]/projects/[:PROJECTID]/issues` (base URL `https://projectsapi.zoho.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-issue.md) for the provider-specific parameters and requirements.

