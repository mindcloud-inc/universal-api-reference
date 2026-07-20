# Nimble: Delete Contact Note

Deletes an existing contact note from Nimble.

```
DELETE https://connect.mindcloud.co/v1/universal/nimble/latest/actions/delete-contact-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nimble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/nimble/latest/actions/delete-contact-note?connectionId=$CONNECTION_ID&noteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "noteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nimble/latest/actions/delete-contact-note?${params}`, {
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
| `noteId` | string | yes | Nimble note_id path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Nimble API, this operation is `DELETE /api/v1/contacts/notes/:note_id` (base URL `https://app.nimble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-note.md) for the provider-specific parameters and requirements.

