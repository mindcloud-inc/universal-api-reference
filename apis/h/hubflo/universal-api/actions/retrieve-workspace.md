# Hubflo: Retrieve Workspace

Retrieves a workspace from Hubflo by ID.

```
GET https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/retrieve-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hubflo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/retrieve-workspace?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/retrieve-workspace?${params}`, {
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
| `id` | string | yes |  |

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

Through the native Hubflo API, this operation is `GET /workspaces/:id` (base URL `https://app.hubflo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-workspace.md) for the provider-specific parameters and requirements.

