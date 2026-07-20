# Hubflo: Update Workspace

Updates an existing workspace in Hubflo.

```
PUT https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/update-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hubflo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/update-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/update-workspace', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `title` | string | yes |  |
| `subtitle` | string | no |  |
| `welcomeMessage` | string | no |  |
| `chatRoomId` | string | no |  |
| `projectId` | string | no |  |
| `tags` | list<string> | no |  |

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

Through the native Hubflo API, this operation is `PATCH /workspaces/:id` (base URL `https://app.hubflo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-workspace.md) for the provider-specific parameters and requirements.

