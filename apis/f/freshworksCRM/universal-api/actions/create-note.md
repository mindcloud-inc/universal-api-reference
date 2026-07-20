# Freshworks CRM: Create Note

Creates a new note in Freshworks CRM.

```
POST https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "note": {},
  "note.description": "string",
  "note.targetableId": 1,
  "note.targetableType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "note": {},
    "note.description": "string",
    "note.targetableId": 1,
    "note.targetableType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `note` | object | yes |  |
| `note.description` | string | yes |  |
| `note.targetableId` | number | yes |  |
| `note.targetableType` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "note": {
        "collab_context": {
          "hasSlackViewAccess": true,
          "messageId": "string"
        },
        "created_at": "string",
        "creater_id": 1,
        "description": "string",
        "duration": 1,
        "has_access": true,
        "has_mentions": true,
        "html_content": "string",
        "id": 1,
        "targetables": [
          {
            "id": 1,
            "type": "string"
          }
        ],
        "updated_at": "string",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `note.collab_context.hasSlackViewAccess` | boolean |  |
| `note.collab_context.messageId` | string |  |
| `note.created_at` | string |  |
| `note.creater_id` | number |  |
| `note.description` | string |  |
| `note.duration` | number |  |
| `note.has_access` | boolean |  |
| `note.has_mentions` | boolean |  |
| `note.html_content` | string |  |
| `note.id` | number |  |
| `note.targetables[].id` | number |  |
| `note.targetables[].type` | string |  |
| `note.updated_at` | string |  |
| `note.url` | string |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `POST /api/notes` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-note.md) for the provider-specific parameters and requirements.

