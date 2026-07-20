# SureContact: Update Note

Updates an existing note in SureContact.

```
PUT https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/update-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureContact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/update-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "noteUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/update-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "noteUuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | no | The updated note content. |
| `noteUuid` | string | yes | The UUID of the note. |
| `title` | string | no | Optional title for the note. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `created_at` | date |  |
| `title` | string |  |
| `updated_at` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native SureContact API, this operation is `PUT api/v1/public/notes/:note_uuid` (base URL `https://api.surecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-note.md) for the provider-specific parameters and requirements.

