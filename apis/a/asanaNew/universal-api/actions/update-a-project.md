# Asana: Update a project

Updates a project in Asana.

```
PUT https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/update-a-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/update-a-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectGid": "string",
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/update-a-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectGid": "string",
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `optFields[]` | array<string> | no |  |
| `projectGid` | string | yes | Path parameter: project_gid |
| `data` | object | yes |  |

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
      "currentStatus": {},
      "currentStatusUpdate": {},
      "defaultAccessLevel": "string",
      "defaultView": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "dueOn": "2026-05-07T12:00:00.000Z",
      "followers": [
        {
          "gid": "string",
          "name": "Ava Chen",
          "resourceType": "string"
        }
      ],
      "gid": "string",
      "icon": "string",
      "members": [
        {
          "gid": "string",
          "name": "Ava Chen",
          "resourceType": "string"
        }
      ],
      "minimumAccessLevelForCustomization": "string",
      "minimumAccessLevelForSharing": "string",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "notes": "string",
      "owner": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      },
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
| `currentStatus` | object |  |
| `currentStatusUpdate` | object |  |
| `defaultAccessLevel` | string |  |
| `defaultView` | string |  |
| `dueDate` | date |  |
| `dueOn` | date |  |
| `followers[].gid` | string |  |
| `followers[].name` | string |  |
| `followers[].resourceType` | string |  |
| `gid` | string |  |
| `icon` | string |  |
| `members[].gid` | string |  |
| `members[].name` | string |  |
| `members[].resourceType` | string |  |
| `minimumAccessLevelForCustomization` | string |  |
| `minimumAccessLevelForSharing` | string |  |
| `modifiedAt` | date |  |
| `name` | string |  |
| `notes` | string |  |
| `owner.gid` | string |  |
| `owner.name` | string |  |
| `owner.resourceType` | string |  |
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

Through the native Asana API, this operation is `PUT projects/:project_gid` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-project.md) for the provider-specific parameters and requirements.

