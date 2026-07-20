# Whautomate: Update Contact

Updates an existing contact in Whautomate.

```
PUT https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whautomate `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `channel` | string | no |  |
| `contactId` | string | yes |  |
| `customFields` | object | no |  |
| `location` | object | no |  |
| `name` | string | no |  |
| `notes` | string | no |  |
| `phoneNumber` | string | no |  |
| `tags[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "id": "string",
      "lastActivity": "2026-05-07T12:00:00.000Z",
      "location": {},
      "name": "Ava Chen",
      "notes": "string",
      "phoneNumber": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `createdAt` | date |  |
| `customFields` | object |  |
| `id` | string |  |
| `lastActivity` | date |  |
| `location` | object |  |
| `name` | string |  |
| `notes` | string |  |
| `phoneNumber` | string |  |
| `tags` | array<string> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Whautomate API, this operation is `PUT /v1/contacts/{{contactId}}` (base URL `https://api.whautomate.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

