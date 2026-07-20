# Keap: Get Note



```
GET https://connect.mindcloud.co/v1/universal/keap/latest/actions/get-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Keap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/keap/latest/actions/get-note?connectionId=$CONNECTION_ID&contact_id=string&note_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact_id": "string",
  "note_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/keap/latest/actions/get-note?${params}`, {
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
| `contact_id` | string | yes | The unique identifier of the contact. |
| `note_id` | string | yes | The unique identifier of the note. |

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
      "createTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastUpdatedByUserId": "string",
      "text": "string",
      "type": "string",
      "updateTime": "2026-05-07T12:00:00.000Z"
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
| `createTime` | date |  |
| `id` | string |  |
| `lastUpdatedByUserId` | string |  |
| `text` | string |  |
| `type` | string |  |
| `updateTime` | date |  |

## Native endpoint

Through the native Keap API, this operation is `GET /contacts/:contact_id/notes/:note_id` (base URL `https://api.infusionsoft.com/crm/rest/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-note.md) for the provider-specific parameters and requirements.

