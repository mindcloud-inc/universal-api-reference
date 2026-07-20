# Locu: Update Note

Updates an existing note in Locu.

```
PUT https://connect.mindcloud.co/v1/universal/locu/latest/actions/update-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Locu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/locu/latest/actions/update-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/locu/latest/actions/update-note', {
  method: 'PUT',
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
| `id` | string | yes | Note ID |
| `text` | string | no | New text content for the note |
| `icon` | string | no | New icon for the note |
| `color` | string | no | New hex color for the icon |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `folderId` | string | no | New parent folder ID |
| `keepBreaks` | boolean | no | Preserve extra blank lines as empty paragraphs Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "icon": "string",
      "id": "string",
      "markdown": "string",
      "name": "Ava Chen",
      "text": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string | Note icon color |
| `createdAt` | date | Note creation timestamp |
| `icon` | string | Note icon |
| `id` | string | Note ID |
| `markdown` | string | Markdown note content |
| `name` | string | Note title |
| `text` | string | Plain text note content |
| `updatedAt` | date | Note last update timestamp |

## Native endpoint

Through the native Locu API, this operation is `PATCH /notes/:id` (base URL `https://api.locu.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-note.md) for the provider-specific parameters and requirements.

