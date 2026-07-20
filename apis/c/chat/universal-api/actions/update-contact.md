# 2Chat: Update Contact

Updates an existing contact in 2Chat.

```
PUT https://connect.mindcloud.co/v1/universal/chat/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chat/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chat/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactUuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactUuid` | string | yes |  |
| `firstName` | string | no |  |
| `lastName` | string | no |  |
| `profilePicUrl` | string | no |  |
| `channelUuid` | string | no | Move the contact to a specific WhatsApp channel UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "channelUuid": {},
        "details": [
          {
            "createdAt": "2026-05-07T12:00:00.000Z",
            "createdAtTimestamp": "2026-05-07T12:00:00.000Z",
            "id": 1,
            "type": "string",
            "value": "string"
          }
        ],
        "firstName": "Ava",
        "lastName": "Chen",
        "lastUpdated": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen",
        "profilePicUrl": {},
        "uuid": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact.channelUuid` | object |  |
| `contact.details[].createdAt` | date |  |
| `contact.details[].createdAtTimestamp` | date |  |
| `contact.details[].id` | number |  |
| `contact.details[].type` | string |  |
| `contact.details[].value` | string |  |
| `contact.firstName` | string |  |
| `contact.lastName` | string |  |
| `contact.lastUpdated` | date |  |
| `contact.name` | string |  |
| `contact.profilePicUrl` | object |  |
| `contact.uuid` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native 2Chat API, this operation is `PUT /contacts/:contactUuid` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

