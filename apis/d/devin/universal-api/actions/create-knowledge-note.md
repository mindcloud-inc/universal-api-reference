# Devin: Create Knowledge Note

Creates a knowledge note in Devin.

```
POST https://connect.mindcloud.co/v1/universal/devin/latest/actions/create-knowledge-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Devin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/devin/latest/actions/create-knowledge-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "string",
  "name": "Ava Chen",
  "orgId": "string",
  "trigger": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/devin/latest/actions/create-knowledge-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "string",
    "name": "Ava Chen",
    "orgId": "string",
    "trigger": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | yes | Knowledge note body. |
| `name` | string | yes | Knowledge note name. |
| `orgId` | string | yes | Devin organization ID. |
| `trigger` | string | yes | Knowledge note trigger text. |

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

Through the native Devin API, this operation is `POST /v3/organizations/:org_id/knowledge/notes` (base URL `https://api.devin.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-knowledge-note.md) for the provider-specific parameters and requirements.

