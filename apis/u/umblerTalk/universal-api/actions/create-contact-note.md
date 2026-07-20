# Umbler Talk: Create Contact Note

Creates a contact note in Umbler Talk.

```
POST https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/create-contact-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Umbler Talk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/create-contact-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string",
  "id": "string",
  "organizationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/umblerTalk/latest/actions/create-contact-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string",
    "id": "string",
    "organizationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | Note content. |
| `id` | string | yes | The contact ID. |
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

Through the native Umbler Talk API, this operation is `POST /v1/contacts/[:id]/notes/` (base URL `https://app-utalk.umbler.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-note.md) for the provider-specific parameters and requirements.

