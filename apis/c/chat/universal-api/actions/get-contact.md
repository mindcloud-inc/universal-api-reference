# 2Chat: Get Contact

Retrieves a contact from 2Chat.

```
GET https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 2Chat `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactUuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactUuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chat/latest/actions/get-contact?${params}`, {
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
| `contactUuid` | string | yes |  |

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
            "id": "string",
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
| `contact.details[].id` | string |  |
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

Through the native 2Chat API, this operation is `GET /contacts/:contactUuid` (base URL `https://api.p.2chat.io/open`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

