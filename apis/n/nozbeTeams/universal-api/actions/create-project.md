# Nozbe Teams: Create Project

Creates a new project in Nozbe Teams.

```
POST https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "teamId": "string",
  "isOpen": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "teamId": "string",
    "isOpen": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The project name. |
| `teamId` | string | yes | The team that will own the project. |
| `isOpen` | boolean | yes | Whether the project is open. |
| `isTemplate` | boolean | no | Whether the project should be created as a template. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "color": "string",
      "createdAt": 1,
      "description": "string",
      "endedAt": "string",
      "extra": "string",
      "id": "string",
      "isFavorite": true,
      "isOpen": true,
      "isSingleActions": true,
      "isTemplate": true,
      "lastEventAt": 1,
      "lastSeenEventAt": 1,
      "name": "Ava Chen",
      "preferences": "string",
      "sharedTeamId": "string",
      "sidebarPosition": 1,
      "teamColor": "string",
      "teamId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | string |  |
| `color` | string |  |
| `createdAt` | number |  |
| `description` | string |  |
| `endedAt` | string |  |
| `extra` | string |  |
| `id` | string |  |
| `isFavorite` | boolean |  |
| `isOpen` | boolean |  |
| `isSingleActions` | boolean |  |
| `isTemplate` | boolean |  |
| `lastEventAt` | number |  |
| `lastSeenEventAt` | number |  |
| `name` | string |  |
| `preferences` | string |  |
| `sharedTeamId` | string |  |
| `sidebarPosition` | number |  |
| `teamColor` | string |  |
| `teamId` | string |  |

## Native endpoint

Through the native Nozbe Teams API, this operation is `POST /projects` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

