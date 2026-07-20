# Nozbe Personal: Create Project From Template

Creates a new project from a Nozbe Personal template.

```
POST https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/create-project-from-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Personal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/create-project-from-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/create-project-from-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Project template ID to clone. |

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
      "sharedTeamId": "string",
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
| `sharedTeamId` | string |  |
| `teamId` | string |  |

## Native endpoint

Through the native Nozbe Personal API, this operation is `POST /projects/from_template/:id` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project-from-template.md) for the provider-specific parameters and requirements.

