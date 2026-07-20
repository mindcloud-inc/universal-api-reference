# v0: Find Chats

Finds chats in the v0 workspace.

```
GET https://connect.mindcloud.co/v1/universal/v0/latest/actions/find-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a v0 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/v0/latest/actions/find-chats?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/v0/latest/actions/find-chats?${params}`, {
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
| `limit` | number | no |  |
| `offset` | number | no |  |
| `isFavorite` | string | no | Filter chats by whether they are marked as favorites. |
| `vercelProjectId` | string | no |  |
| `branch` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "apiUrl": "https://example.com",
      "authorId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "favorite": true,
      "id": "string",
      "latestVersion": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "demoUrl": "https://example.com",
        "id": "string",
        "object": "string",
        "status": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z"
      },
      "name": "Ava Chen",
      "object": "string",
      "privacy": "string",
      "projectId": "string",
      "shareable": true,
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
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
| `authorId` | string |  |
| `createdAt` | date |  |
| `favorite` | boolean |  |
| `id` | string |  |
| `latestVersion.createdAt` | date |  |
| `latestVersion.demoUrl` | string |  |
| `latestVersion.id` | string |  |
| `latestVersion.object` | string |  |
| `latestVersion.status` | string |  |
| `latestVersion.updatedAt` | date |  |
| `name` | string |  |
| `object` | string |  |
| `privacy` | string |  |
| `projectId` | string |  |
| `shareable` | boolean |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `webUrl` | string |  |

## Native endpoint

Through the native v0 API, this operation is `GET /v1/chats` (base URL `https://api.v0.dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/find-chats.md) for the provider-specific parameters and requirements.

