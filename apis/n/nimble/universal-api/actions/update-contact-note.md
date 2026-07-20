# Nimble: Update Contact Note

Updates an existing note for Nimble contacts.

```
PUT https://connect.mindcloud.co/v1/universal/nimble/latest/actions/update-contact-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nimble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nimble/latest/actions/update-contact-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "noteId": "string",
  "contactIds[]": [
    "string"
  ],
  "note": "string",
  "notePreview": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nimble/latest/actions/update-contact-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "noteId": "string",
    "contactIds[]": ["string"],
    "note": "string",
    "notePreview": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `noteId` | string | yes | Nimble note_id path parameter. |
| `contactIds[]` | array<string> | yes |  |
| `note` | string | yes |  |
| `notePreview` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorName": "Ava Chen",
      "contacts": [
        [
          {}
        ]
      ],
      "created": "string",
      "id": "string",
      "note": "string",
      "notePreview": "string",
      "owner": {
        "avatarUrl": "https://example.com",
        "email": "ava@example.com",
        "isActive": true,
        "name": "Ava Chen",
        "userId": "string"
      },
      "ownerId": "string",
      "updated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorName` | string |  |
| `contacts[]` | array<object> |  |
| `contacts[].avatarUrl` | string |  |
| `contacts[].contactType` | string |  |
| `contacts[].email[]` | array<string> |  |
| `contacts[].id` | string |  |
| `contacts[].isViewable` | boolean |  |
| `contacts[].name` | string |  |
| `contacts[].phones[]` | array<string> |  |
| `created` | string |  |
| `id` | string |  |
| `note` | string |  |
| `notePreview` | string |  |
| `owner` | object |  |
| `owner.avatarUrl` | string |  |
| `owner.email` | string |  |
| `owner.isActive` | boolean |  |
| `owner.name` | string |  |
| `owner.userId` | string |  |
| `ownerId` | string |  |
| `updated` | string |  |

## Native endpoint

Through the native Nimble API, this operation is `PUT /api/v1/contacts/notes/:note_id` (base URL `https://app.nimble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact-note.md) for the provider-specific parameters and requirements.

