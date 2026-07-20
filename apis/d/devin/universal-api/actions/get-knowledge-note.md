# Devin: Get Knowledge Note

Retrieves a knowledge note from Devin.

```
GET https://connect.mindcloud.co/v1/universal/devin/latest/actions/get-knowledge-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Devin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devin/latest/actions/get-knowledge-note?connectionId=$CONNECTION_ID&noteId=string&orgId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "noteId": "string",
  "orgId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devin/latest/actions/get-knowledge-note?${params}`, {
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
| `noteId` | string | yes | Knowledge note ID. |
| `orgId` | string | yes | Devin organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "access_type": "string",
      "body": "string",
      "created_at": 1,
      "folder_id": "string",
      "folder_path": "string",
      "is_enabled": true,
      "name": "Ava Chen",
      "note_id": "string",
      "org_id": "string",
      "trigger": "string",
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_type` | string | Access scope. |
| `body` | string | Knowledge note body. |
| `created_at` | number | Creation timestamp. |
| `folder_id` | string | Folder ID when returned. |
| `folder_path` | string | Folder path. |
| `is_enabled` | boolean | Whether the note is enabled. |
| `name` | string | Knowledge note name. |
| `note_id` | string | Knowledge note ID. |
| `org_id` | string | Organization ID. |
| `trigger` | string | Knowledge note trigger. |
| `updated_at` | number | Update timestamp. |

## Native endpoint

Through the native Devin API, this operation is `GET /v3/organizations/:org_id/knowledge/notes/:note_id` (base URL `https://api.devin.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-knowledge-note.md) for the provider-specific parameters and requirements.

