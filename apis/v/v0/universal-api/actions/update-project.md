# v0: Update Project

Updates an existing project in v0.

```
PUT https://connect.mindcloud.co/v1/universal/v0/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a v0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/v0/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/v0/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | The ID of the project to update. |
| `name` | string | no |  |
| `description` | string | no |  |
| `instructions` | string | no |  |
| `privacy` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiUrl": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "instructions": "string",
      "name": "Ava Chen",
      "object": "string",
      "privacy": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "vercelProjectId": "string",
      "webUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiUrl` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `instructions` | string |  |
| `name` | string |  |
| `object` | string |  |
| `privacy` | string |  |
| `updatedAt` | date |  |
| `vercelProjectId` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native v0 API, this operation is `PATCH /v1/projects/:projectId` (base URL `https://api.v0.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

