# Sakari SMS: Get Conversation by ID

Retrieves a conversation from Sakari SMS.

```
GET https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/get-conversation-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sakari SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/get-conversation-by-id?connectionId=$CONNECTION_ID&conversationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/get-conversation-by-id?${params}`, {
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
| `conversationId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "closed": "2026-05-07T12:00:00.000Z",
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
      "id": "string",
      "lastMessage": {
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
        "conversation": {
          "closed": "2026-05-07T12:00:00.000Z",
          "contact": {},
          "created": {},
          "group": {},
          "id": "string",
          "lastMessage": {},
          "phoneNumber": {},
          "type": "string",
          "unread": [
            "string"
          ],
          "updated": {}
        },
        "group": {
          "id": "string",
          "name": "Ava Chen",
          "notifications": [
            {}
          ],
          "phoneNumbers": [
            {}
          ],
          "senders": [
            {}
          ],
          "tags": [
            "string"
          ],
          "users": [
            {}
          ]
        },
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `closed` | date |  |
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
| `id` | string |  |
| `lastMessage` | object |  |
| `lastMessage.contact` | object |  |
| `lastMessage.contact.activecampaign` | object |  |
| `lastMessage.contact.attributes` | object |  |
| `lastMessage.contact.blocked` | date |  |
| `lastMessage.contact.created` | object |  |
| `lastMessage.contact.email` | string |  |
| `lastMessage.contact.error` | object |  |
| `lastMessage.contact.firstName` | string |  |
| `lastMessage.contact.hubspot` | object |  |
| `lastMessage.contact.id` | string |  |
| `lastMessage.contact.lastName` | string |  |
| `lastMessage.contact.lists` | array<object> |  |
| `lastMessage.contact.mobile` | object |  |
| `lastMessage.contact.optIn` | date |  |
| `lastMessage.contact.pipedrive` | object |  |
| `lastMessage.contact.updated` | object |  |
| `lastMessage.contact.valid` | boolean |  |
| `lastMessage.conversation` | object |  |
| `lastMessage.conversation.closed` | date |  |
| `lastMessage.conversation.contact` | object |  |
| `lastMessage.conversation.created` | object |  |
| `lastMessage.conversation.group` | object |  |
| `lastMessage.conversation.id` | string |  |
| `lastMessage.conversation.lastMessage` | object |  |
| `lastMessage.conversation.phoneNumber` | object |  |
| `lastMessage.conversation.type` | string |  |
| `lastMessage.conversation.unread` | array<string> |  |
| `lastMessage.conversation.updated` | object |  |
| `lastMessage.group` | object |  |
| `lastMessage.group.id` | string |  |
| `lastMessage.group.name` | string |  |
| `lastMessage.group.notifications` | array<object> |  |
| `lastMessage.group.phoneNumbers` | array<object> |  |
| `lastMessage.group.senders` | array<object> |  |
| `lastMessage.group.tags` | array<string> |  |
| `lastMessage.group.users` | array<object> |  |
| `lastMessage.id` | string |  |

## Native endpoint

Through the native Sakari SMS API, this operation is `GET /v1/accounts/:accountId/conversations/:conversationId` (base URL `https://api.sakari.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation-by-id.md) for the provider-specific parameters and requirements.

