# Keap: Update Note



```
PUT https://connect.mindcloud.co/v1/universal/keap/latest/actions/update-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/keap/latest/actions/update-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contact_id": "string",
  "note_id": "string",
  "user_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/keap/latest/actions/update-note', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contact_id": "string",
    "note_id": "string",
    "user_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact_id` | string | yes | The unique identifier of the contact. |
| `is_pinned` | string | no |  |
| `note_id` | string | yes | The unique identifier of the note. |
| `text` | string | no |  |
| `title` | string | no |  |
| `type` | string | no |  |
| `update_mask` | string | no |  |
| `user_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedToUser": {
        "emailAddress": "ava@example.com",
        "familyName": "Ava Chen",
        "givenName": "Ava Chen",
        "id": "string"
      },
      "contactId": "string",
      "createdByUserId": "string",
      "createTime": "string",
      "id": "string",
      "lastUpdatedByUserId": "string",
      "pinnedAt": "string",
      "text": "string",
      "title": "string",
      "type": "string",
      "updateTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedToUser.emailAddress` | string |  |
| `assignedToUser.familyName` | string |  |
| `assignedToUser.givenName` | string |  |
| `assignedToUser.id` | string |  |
| `contactId` | string |  |
| `createdByUserId` | string |  |
| `createTime` | string |  |
| `id` | string |  |
| `lastUpdatedByUserId` | string |  |
| `pinnedAt` | string |  |
| `text` | string |  |
| `title` | string |  |
| `type` | string |  |
| `updateTime` | string |  |

## Native endpoint

Through the native Keap API, this operation is `PATCH /contacts/{contact_id}/notes/{note_id}` (base URL `https://api.infusionsoft.com/crm/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-note.md) for the provider-specific parameters and requirements.

