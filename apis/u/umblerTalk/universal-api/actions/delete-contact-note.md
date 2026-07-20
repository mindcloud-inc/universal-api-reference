# Umbler Talk: Delete Contact Note

Deletes a contact note from Umbler Talk.

```
DELETE https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/delete-contact-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbler Talk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/delete-contact-note?connectionId=$CONNECTION_ID&id=string&noteId=string&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "noteId": "string",
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/delete-contact-note?${params}`, {
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
| `id` | string | yes | The contact ID. |
| `noteId` | string | yes | The note ID. |
| `organizationId` | string | yes | The organization ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_t": "string",
      "channelIds": [
        "string"
      ],
      "contactType": "string",
      "createdAtUTC": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {}
      ],
      "email": "ava@example.com",
      "id": "string",
      "isBlocked": true,
      "name": "Ava Chen",
      "notes": [
        {}
      ],
      "phoneNumber": "string",
      "profilePictureUrl": "https://example.com",
      "tags": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_t` | string |  |
| `channelIds` | array<string> |  |
| `contactType` | string |  |
| `createdAtUTC` | date |  |
| `customFields` | array<object> |  |
| `email` | string |  |
| `id` | string |  |
| `isBlocked` | boolean |  |
| `name` | string |  |
| `notes` | array<object> |  |
| `phoneNumber` | string |  |
| `profilePictureUrl` | string |  |
| `tags` | array<object> |  |

## Native endpoint

Through the native Umbler Talk API, this operation is `DELETE /v1/contacts/[:id]/notes/[:noteId]/` (base URL `https://app-utalk.umbler.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contact-note.md) for the provider-specific parameters and requirements.

