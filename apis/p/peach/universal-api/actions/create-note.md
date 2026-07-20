# Peach: Create Note

Creates a note for a contact in Peach.

```
POST https://connect.mindcloud.co/v1/universal/peach/latest/actions/create-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Peach `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/peach/latest/actions/create-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string",
  "noteBody": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/peach/latest/actions/create-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string",
    "noteBody": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | string | yes | The contact ID that should receive the note. |
| `noteTitle` | string | no | Optional title for the note. |
| `noteBody` | string | yes | The note content. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "interactionResponse": "string",
      "noteBody": {
        "category": "string",
        "contactId": "string",
        "noteBody": "string",
        "noteTitle": "string",
        "source": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `interactionResponse` | string |  |
| `noteBody` | object |  |
| `noteBody.category` | string |  |
| `noteBody.contactId` | string |  |
| `noteBody.noteBody` | string |  |
| `noteBody.noteTitle` | string |  |
| `noteBody.source` | string |  |

## Native endpoint

Through the native Peach API, this operation is `POST /notes` (base URL `https://api.peach-in.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-note.md) for the provider-specific parameters and requirements.

