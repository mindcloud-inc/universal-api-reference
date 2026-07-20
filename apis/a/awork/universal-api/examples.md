# Awork Universal API Examples

These examples use the MindCloud API key and Awork connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Awork.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/awork/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/awork/latest/actions/get-current-user?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "createdBy": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "firstName": "Ava",
      "hasImage": true,
      "id": "string",
      "isArchived": true,
      "isDeactivated": true,
      "isExternal": true,
      "language": "string",
      "lastName": "Chen",
      "resourceVersion": 1,
      "shouldMigrateToConnect": true,
      "status": {
        "invitationAccepted": true,
        "isDeactivated": true
      },
      "updatedBy": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z",
      "userContactInfos": [
        {
          "createdBy": "string",
          "createdOn": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "isAddress": true,
          "subType": "string",
          "type": "string",
          "updatedBy": "string",
          "updatedOn": "2026-05-07T12:00:00.000Z",
          "value": "string"
        }
      ],
      "workspace": {
        "id": "string",
        "name": "Ava Chen",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/awork/latest/actions/get-current-user).

## Create Project

Creates a project in Awork.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/awork/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud API project validation 2026-03-20"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/awork/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud API project validation 2026-03-20"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "createdBy": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "deductNonBillableHours": true,
      "description": "string",
      "hasImage": true,
      "id": "string",
      "isBillableByDefault": true,
      "isExternal": true,
      "isMultiAssignmentAllowed": true,
      "isPrivate": true,
      "isRetainer": true,
      "name": "Ava Chen",
      "plannedDuration": 1,
      "projectKey": "string",
      "projectStatus": {
        "id": "string",
        "isArchived": true,
        "isExternal": true,
        "name": "Ava Chen",
        "type": "string",
        "typeOrder": 1
      },
      "projectStatusId": "string",
      "resourceVersion": 1,
      "tasksCount": 1,
      "tasksDoneCount": 1,
      "timeBudget": 1,
      "totalPlannedDurationWithHierarchy": 1,
      "trackedDuration": 1,
      "updatedBy": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Project action reference](actions/create-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/awork/latest/actions/create-project).
