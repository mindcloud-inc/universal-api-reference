# Hubflo: List Workspaces

Retrieves all workspace records from Hubflo.

```
GET https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/list-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hubflo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/list-workspaces?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/list-workspaces?${params}`, {
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
| `page` | number | no |  |
| `perPage` | number | no |  |
| `projectId` | string | no |  |
| `workspaceId` | string | no |  |
| `title` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "chat_room_id": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "project_id": "string",
      "subtitle": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "welcome_message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `chat_room_id` | string |  |
| `created_at` | date |  |
| `id` | string |  |
| `project_id` | string |  |
| `subtitle` | string |  |
| `tags` | array<string> |  |
| `title` | string |  |
| `welcome_message` | string |  |

## Native endpoint

Through the native Hubflo API, this operation is `GET /workspaces` (base URL `https://app.hubflo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workspaces.md) for the provider-specific parameters and requirements.

