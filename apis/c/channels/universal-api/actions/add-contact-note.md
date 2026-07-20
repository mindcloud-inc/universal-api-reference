# Channels: Add Contact Note

Creates a contact note in Channels.

```
POST https://connect.mindcloud.co/v1/universal/channels/latest/actions/add-contact-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/channels/latest/actions/add-contact-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": 1,
  "note": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/channels/latest/actions/add-contact-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": 1,
    "note": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactId` | number | yes | Contact ID to add the note to. |
| `note` | string | yes | Contents of the note. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "alternativeMsisdns": [
        "string"
      ],
      "contactId": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": 1,
      "lastModificationDate": "2026-05-07T12:00:00.000Z",
      "lock": "string",
      "origin": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `alternativeMsisdns[]` | string |  |
| `contactId` | number |  |
| `createdAt` | date |  |
| `createdBy` | number |  |
| `lastModificationDate` | date |  |
| `lock` | string |  |
| `origin` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Channels API, this operation is `POST /api/v1/contacts/{contactId}/note` (base URL `https://api.channels.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-contact-note.md) for the provider-specific parameters and requirements.

