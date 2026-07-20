# Nozbe Personal: List Projects

Retrieves accessible projects from Nozbe Personal.

```
GET https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Personal `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/list-projects?${params}`, {
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
| `sortBy` | string | no | Comma-separated sort expression. |
| `teamId` | string | no | Filter projects by team. |
| `isSingleActions` | boolean | no | Filter by single-task projects. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "extra": "string",
      "id": "string",
      "isFavorite": true,
      "isOpen": true,
      "isSingleActions": true,
      "isTemplate": true,
      "lastEventAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "sharedTeamId": {},
      "sidebarPosition": 1,
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
| `createdAt` | date |  |
| `extra` | string |  |
| `id` | string |  |
| `isFavorite` | boolean |  |
| `isOpen` | boolean |  |
| `isSingleActions` | boolean |  |
| `isTemplate` | boolean |  |
| `lastEventAt` | date |  |
| `name` | string |  |
| `sharedTeamId` | object |  |
| `sidebarPosition` | number |  |
| `teamId` | string |  |

## Native endpoint

Through the native Nozbe Personal API, this operation is `GET /projects` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

