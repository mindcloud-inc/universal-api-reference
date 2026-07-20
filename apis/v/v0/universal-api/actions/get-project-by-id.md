# v0: Get Project by ID

Retrieves a project from v0 by ID.

```
GET https://connect.mindcloud.co/v1/universal/v0/latest/actions/get-project-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a v0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/v0/latest/actions/get-project-by-id?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/v0/latest/actions/get-project-by-id?${params}`, {
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
| `projectId` | string | yes | The ID of the project to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiUrl": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
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
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `privacy` | string |  |
| `updatedAt` | date |  |
| `vercelProjectId` | string |  |
| `webUrl` | string |  |

## Native endpoint

Through the native v0 API, this operation is `GET /v1/projects/:projectId` (base URL `https://api.v0.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-by-id.md) for the provider-specific parameters and requirements.

