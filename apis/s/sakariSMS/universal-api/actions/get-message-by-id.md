# Sakari SMS: Get Message by ID

Retrieves a message from Sakari SMS.

```
GET https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/get-message-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sakari SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/get-message-by-id?connectionId=$CONNECTION_ID&messageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/get-message-by-id?${params}`, {
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
| `messageId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "activecampaign": {
          "id": 1
        },
        "attributes": {},
        "blocked": "2026-05-07T12:00:00.000Z",
        "created": {
          "at": "2026-05-07T12:00:00.000Z",
          "by": {}
        },
        "email": "ava@example.com",
        "error": {
          "code": "string",
          "description": "string"
        },
        "firstName": "Ava",
        "hubspot": {
          "id": 1
        },
        "id": "string",
        "lastName": "Chen",
        "lists": {
          "lists": [
            {
              "doubleOptIn": {},
              "filter": {},
              "id": "string",
              "keyword": "string",
              "name": "Ava Chen",
              "optIn": "2026-05-07T12:00:00.000Z",
              "optInConfirmation": "string",
              "optOut": "2026-05-07T12:00:00.000Z",
              "source": {}
            }
          ]
        },
        "mobile": {
          "country": "string",
          "lineType": "string",
          "number": "string",
          "valid": true,
          "verified": "2026-05-07T12:00:00.000Z"
        },
        "optIn": "2026-05-07T12:00:00.000Z",
        "pipedrive": {
          "id": 1
        },
        "updated": {
          "at": "2026-05-07T12:00:00.000Z",
          "by": {}
        },
        "valid": true
      },
      "conversation": {
        "closed": "2026-05-07T12:00:00.000Z",
        "contact": {
          "activecampaign": {},
          "attributes": {},
          "blocked": "2026-05-07T12:00:00.000Z",
          "created": {},
          "email": "ava@example.com",
          "error": {},
          "firstName": "Ava",
          "hubspot": {},
          "id": "string",
          "lastName": "Chen",
          "lists": [
            {}
          ],
          "mobile": {},
          "optIn": "2026-05-07T12:00:00.000Z",
          "pipedrive": {},
          "updated": {},
          "valid": true
        },
        "id": "string",
        "lastMessage": {
          "contact": {},
          "conversation": {},
          "created": {},
          "error": {},
          "group": {},
          "id": "string",
          "media": [
            {}
          ],
          "message": "string",
          "outgoing": true,
          "phoneNumber": "string",
          "price": 1,
          "read": true,
          "segments": 1,
          "sendAt": "2026-05-07T12:00:00.000Z",
          "status": "string",
          "template": "string",
          "type": "string",
          "updated": {}
        }
      },
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact` | object |  |
| `contact.activecampaign` | object |  |
| `contact.activecampaign.id` | number |  |
| `contact.attributes` | object |  |
| `contact.blocked` | date |  |
| `contact.created` | object |  |
| `contact.created.at` | date |  |
| `contact.created.by` | object |  |
| `contact.email` | string |  |
| `contact.error` | object |  |
| `contact.error.code` | string |  |
| `contact.error.description` | string |  |
| `contact.firstName` | string |  |
| `contact.hubspot` | object |  |
| `contact.hubspot.id` | number |  |
| `contact.id` | string |  |
| `contact.lastName` | string |  |
| `contact.lists` | array<object> |  |
| `contact.lists.lists[].doubleOptIn` | object |  |
| `contact.lists.lists[].filter` | object |  |
| `contact.lists.lists[].id` | string |  |
| `contact.lists.lists[].keyword` | string |  |
| `contact.lists.lists[].name` | string |  |
| `contact.lists.lists[].optIn` | date |  |
| `contact.lists.lists[].optInConfirmation` | string |  |
| `contact.lists.lists[].optOut` | date |  |
| `contact.lists.lists[].source` | object |  |
| `contact.mobile` | object |  |
| `contact.mobile.country` | string |  |
| `contact.mobile.lineType` | string |  |
| `contact.mobile.number` | string |  |
| `contact.mobile.valid` | boolean |  |
| `contact.mobile.verified` | date |  |
| `contact.optIn` | date |  |
| `contact.pipedrive` | object |  |
| `contact.pipedrive.id` | number |  |
| `contact.updated` | object |  |
| `contact.updated.at` | date |  |
| `contact.updated.by` | object |  |
| `contact.valid` | boolean |  |
| `conversation` | object |  |
| `conversation.closed` | date |  |
| `conversation.contact` | object |  |
| `conversation.contact.activecampaign` | object |  |
| `conversation.contact.attributes` | object |  |
| `conversation.contact.blocked` | date |  |
| `conversation.contact.created` | object |  |
| `conversation.contact.email` | string |  |
| `conversation.contact.error` | object |  |
| `conversation.contact.firstName` | string |  |
| `conversation.contact.hubspot` | object |  |
| `conversation.contact.id` | string |  |
| `conversation.contact.lastName` | string |  |
| `conversation.contact.lists` | array<object> |  |
| `conversation.contact.mobile` | object |  |
| `conversation.contact.optIn` | date |  |
| `conversation.contact.pipedrive` | object |  |
| `conversation.contact.updated` | object |  |
| `conversation.contact.valid` | boolean |  |
| `conversation.id` | string |  |
| `conversation.lastMessage` | object |  |
| `conversation.lastMessage.contact` | object |  |
| `conversation.lastMessage.conversation` | object |  |
| `conversation.lastMessage.created` | object |  |
| `conversation.lastMessage.error` | object |  |
| `conversation.lastMessage.group` | object |  |
| `conversation.lastMessage.id` | string |  |
| `conversation.lastMessage.media` | array<object> | List of media objects attached to message |
| `conversation.lastMessage.message` | string |  |
| `conversation.lastMessage.outgoing` | boolean |  |
| `conversation.lastMessage.phoneNumber` | string |  |
| `conversation.lastMessage.price` | number |  |
| `conversation.lastMessage.read` | boolean |  |
| `conversation.lastMessage.segments` | number |  |
| `conversation.lastMessage.sendAt` | date |  |
| `conversation.lastMessage.status` | string |  |
| `conversation.lastMessage.template` | string |  |
| `conversation.lastMessage.type` | string |  |
| `conversation.lastMessage.updated` | object |  |
| `id` | string |  |

## Native endpoint

Through the native Sakari SMS API, this operation is `GET /v1/accounts/:accountId/messages/:messageId` (base URL `https://api.sakari.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message-by-id.md) for the provider-specific parameters and requirements.

