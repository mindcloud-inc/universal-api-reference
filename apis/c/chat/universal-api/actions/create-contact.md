# 2Chat: Create Contact

Creates a new contact in 2Chat.

```
POST https://connect.mindcloud.co/v1/universal/chat/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chat/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "contactDetail[]": [
    {}
  ],
  "contactDetail[].type": "string",
  "contactDetail[].value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chat/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "contactDetail[]": [{}],
    "contactDetail[].type": "string",
    "contactDetail[].value": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes |  |
| `lastName` | string | no |  |
| `profilePicUrl` | string | no |  |
| `channelUuid` | string | no | Assign the contact to a specific WhatsApp channel UUID. |
| `contactDetail[]` | array<object> | yes | Provide at least one contact method such as a phone number or email address. |
| `contactDetail[].type` | string | yes |  |
| `contactDetail[].value` | string | yes |  |
| `customField[]` | array<object> | no | Optional custom field entries stored on the contact. |
| `customField[].title` | string | no |  |
| `customField[].value` | string | no |  |

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

Through the native 2Chat API, this operation is `POST /contacts` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

