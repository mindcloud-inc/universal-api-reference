# Asana: Remove users from a project

Removes users from a project in Asana.

```
PUT https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/remove-users-from-a-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/remove-users-from-a-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "dataMembers": "string",
  "projectGid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/remove-users-from-a-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "dataMembers": "string",
    "projectGid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dataMembers` | string | yes |  |
| `projectGid` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "color": {},
      "completed": true,
      "completedAt": "2026-05-07T12:00:00.000Z",
      "completedBy": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currentStatus": {
        "author": {
          "gid": "string",
          "name": "Ava Chen",
          "resourceType": "string"
        },
        "color": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "createdBy": {
          "gid": "string",
          "name": "Ava Chen",
          "resourceType": "string"
        },
        "gid": "string",
        "modifiedAt": "2026-05-07T12:00:00.000Z",
        "text": "string",
        "title": "string"
      },
      "currentStatusUpdate": {
        "gid": "string",
        "resourceSubtype": "string",
        "resourceType": "string",
        "title": "string"
      },
      "defaultAccessLevel": "string",
      "defaultView": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "dueOn": "2026-05-07T12:00:00.000Z",
      "gid": "string",
      "icon": "string",
      "minimumAccessLevelForCustomization": "string",
      "minimumAccessLevelForSharing": "string",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "notes": "string",
      "owner": {},
      "permalinkUrl": "https://example.com",
      "privacySetting": "string",
      "public": true,
      "resourceType": "string",
      "startOn": "2026-05-07T12:00:00.000Z",
      "team": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      },
      "workspace": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `color` | object |  |
| `completed` | boolean |  |
| `completedAt` | date |  |
| `completedBy` | object |  |
| `createdAt` | date |  |
| `currentStatus.author.gid` | string |  |
| `currentStatus.author.name` | string |  |
| `currentStatus.author.resourceType` | string |  |
| `currentStatus.color` | string |  |
| `currentStatus.createdAt` | date |  |
| `currentStatus.createdBy.gid` | string |  |
| `currentStatus.createdBy.name` | string |  |
| `currentStatus.createdBy.resourceType` | string |  |
| `currentStatus.gid` | string |  |
| `currentStatus.modifiedAt` | date |  |
| `currentStatus.text` | string |  |
| `currentStatus.title` | string |  |
| `currentStatusUpdate.gid` | string |  |
| `currentStatusUpdate.resourceSubtype` | string |  |
| `currentStatusUpdate.resourceType` | string |  |
| `currentStatusUpdate.title` | string |  |
| `defaultAccessLevel` | string |  |
| `defaultView` | string |  |
| `dueDate` | date |  |
| `dueOn` | date |  |
| `gid` | string |  |
| `icon` | string |  |
| `minimumAccessLevelForCustomization` | string |  |
| `minimumAccessLevelForSharing` | string |  |
| `modifiedAt` | date |  |
| `name` | string |  |
| `notes` | string |  |
| `owner` | object |  |
| `permalinkUrl` | string |  |
| `privacySetting` | string |  |
| `public` | boolean |  |
| `resourceType` | string |  |
| `startOn` | date |  |
| `team.gid` | string |  |
| `team.name` | string |  |
| `team.resourceType` | string |  |
| `workspace.gid` | string |  |
| `workspace.name` | string |  |
| `workspace.resourceType` | string |  |

## Native endpoint

Through the native Asana API, this operation is `POST projects/:project_gid/removeMembers` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-users-from-a-project.md) for the provider-specific parameters and requirements.

