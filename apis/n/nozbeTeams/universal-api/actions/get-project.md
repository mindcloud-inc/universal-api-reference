# Nozbe Teams: Get Project

Retrieves a project from Nozbe Teams.

```
GET https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/get-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/get-project?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/get-project?${params}`, {
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
| `id` | string | yes | The Nozbe project ID. |

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

Through the native Nozbe Teams API, this operation is `GET /projects/:id` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project.md) for the provider-specific parameters and requirements.

