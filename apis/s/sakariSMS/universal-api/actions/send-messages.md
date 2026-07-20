# Sakari SMS: Send Messages

Sends text messages through Sakari SMS.

```
POST https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/send-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sakari SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/send-messages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sakariSMS/latest/actions/send-messages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversations[]` | array<string> | no | List of conversation ids to send messages to |
| `contacts[]` | array<object> | no |  |
| `contacts.contacts[].id` | string | no |  |
| `contacts.contacts[].email` | string | no |  |
| `contacts.contacts[].firstName` | string | no |  |
| `contacts.contacts[].lastName` | string | no |  |
| `contacts.contacts[].mobile` | object | no |  |
| `contacts.contacts[].mobile.country` | string | no |  |
| `contacts.contacts[].mobile.number` | string | no |  |
| `contacts.contacts[].mobile.verified` | date | no |  |
| `contacts.contacts[].mobile.valid` | boolean | no |  |
| `contacts.contacts[].mobile.lineType` | string | no |  |
| `contacts.contacts[].lists[]` | array<object> | no |  |
| `contacts.contacts[].lists.lists[].id` | string | no |  |
| `contacts.contacts[].lists.lists[].name` | string | no |  |
| `contacts.contacts[].lists.lists[].source` | object | no |  |
| `contacts.contacts[].lists.lists[].keyword` | string | no |  |
| `contacts.contacts[].lists.lists[].doubleOptIn` | object | no |  |
| `contacts.contacts[].lists.lists[].filter` | object | no |  |
| `contacts.contacts[].lists.lists[].optInConfirmation` | string | no |  |
| `contacts.contacts[].lists.lists[].optIn` | date | no |  |
| `contacts.contacts[].lists.lists[].optOut` | date | no |  |
| `contacts.contacts[].attributes` | object | no |  |
| `contacts.contacts[].optIn` | date | no |  |
| `contacts.contacts[].blocked` | date | no |  |
| `contacts.contacts[].activecampaign` | object | no |  |
| `contacts.contacts[].activecampaign.id` | number | no |  |
| `contacts.contacts[].hubspot` | object | no |  |
| `contacts.contacts[].hubspot.id` | number | no |  |
| `contacts.contacts[].pipedrive` | object | no |  |
| `contacts.contacts[].pipedrive.id` | number | no |  |
| `contacts.contacts[].valid` | boolean | no |  |
| `contacts.contacts[].error` | object | no |  |
| `contacts.contacts[].error.code` | string | no |  |
| `contacts.contacts[].error.description` | string | no |  |
| `contacts.contacts[].created` | object | no |  |
| `contacts.contacts[].created.at` | date | no |  |
| `contacts.contacts[].created.by` | object | no |  |
| `contacts.contacts[].updated` | object | no |  |
| `contacts.contacts[].updated.at` | date | no |  |
| `contacts.contacts[].updated.by` | object | no |  |
| `filters` | object | no |  |
| `filters.tags[]` | array<string> | no |  |
| `filters.attributes[]` | array<object> | no |  |
| `phoneNumberFilter` | object | no |  |
| `phoneNumberFilter.group` | object | no |  |
| `phoneNumberFilter.group.id` | string | no |  |
| `template` | string | no |  |
| `type` | string | no |  |
| `media[]` | array<object> | no | List of media objects to attach to message |
| `media.media[].url` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invalid": {
        "invalid": [
          {
            "email": "ava@example.com",
            "firstName": "Ava",
            "id": "string",
            "lastName": "Chen",
            "lists": [
              {}
            ],
            "mobile": {
              "country": "string",
              "lineType": "string",
              "number": "string",
              "valid": true,
              "verified": "2026-05-07T12:00:00.000Z"
            }
          }
        ]
      },
      "jobId": "string",
      "messages": {
        "messages": [
          {
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
            "created": {
              "at": "2026-05-07T12:00:00.000Z",
              "by": {}
            },
            "error": {
              "code": "string",
              "description": "string"
            },
            "group": {
              "id": "string",
              "isDefault": true,
              "name": "Ava Chen",
              "notifications": [
                {}
              ],
              "officeHours": {},
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
              ],
              "useSharedPool": true
            },
            "id": "string",
            "media": {
              "media": [
                {
                  "filename": "Ava Chen",
                  "name": "Ava Chen",
                  "type": "string",
                  "url": "https://example.com"
                }
              ]
            },
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
            "updated": {
              "at": "2026-05-07T12:00:00.000Z",
              "by": {}
            }
          }
        ]
      },
      "requested": 1,
      "valid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invalid` | array<object> |  |
| `invalid.invalid[].email` | string |  |
| `invalid.invalid[].firstName` | string |  |
| `invalid.invalid[].id` | string |  |
| `invalid.invalid[].lastName` | string |  |
| `invalid.invalid[].lists` | array<object> |  |
| `invalid.invalid[].mobile` | object |  |
| `invalid.invalid[].mobile.country` | string |  |
| `invalid.invalid[].mobile.lineType` | string |  |
| `invalid.invalid[].mobile.number` | string |  |
| `invalid.invalid[].mobile.valid` | boolean |  |
| `invalid.invalid[].mobile.verified` | date |  |
| `jobId` | string |  |
| `messages` | array<object> |  |
| `messages.messages[].contact` | object |  |
| `messages.messages[].contact.activecampaign` | object |  |
| `messages.messages[].contact.attributes` | object |  |
| `messages.messages[].contact.blocked` | date |  |
| `messages.messages[].contact.created` | object |  |
| `messages.messages[].contact.email` | string |  |
| `messages.messages[].contact.error` | object |  |
| `messages.messages[].contact.firstName` | string |  |
| `messages.messages[].contact.hubspot` | object |  |
| `messages.messages[].contact.id` | string |  |
| `messages.messages[].contact.lastName` | string |  |
| `messages.messages[].contact.lists` | array<object> |  |
| `messages.messages[].contact.mobile` | object |  |
| `messages.messages[].contact.optIn` | date |  |
| `messages.messages[].contact.pipedrive` | object |  |
| `messages.messages[].contact.updated` | object |  |
| `messages.messages[].contact.valid` | boolean |  |
| `messages.messages[].conversation` | object |  |
| `messages.messages[].conversation.closed` | date |  |
| `messages.messages[].conversation.contact` | object |  |
| `messages.messages[].conversation.created` | object |  |
| `messages.messages[].conversation.group` | object |  |
| `messages.messages[].conversation.id` | string |  |
| `messages.messages[].conversation.lastMessage` | object |  |
| `messages.messages[].conversation.phoneNumber` | object |  |
| `messages.messages[].conversation.type` | string |  |
| `messages.messages[].conversation.unread` | array<string> |  |
| `messages.messages[].conversation.updated` | object |  |
| `messages.messages[].created` | object |  |
| `messages.messages[].created.at` | date |  |
| `messages.messages[].created.by` | object |  |
| `messages.messages[].error` | object |  |
| `messages.messages[].error.code` | string |  |
| `messages.messages[].error.description` | string |  |
| `messages.messages[].group` | object |  |
| `messages.messages[].group.id` | string |  |
| `messages.messages[].group.isDefault` | boolean |  |
| `messages.messages[].group.name` | string |  |
| `messages.messages[].group.notifications` | array<object> |  |
| `messages.messages[].group.officeHours` | object |  |
| `messages.messages[].group.phoneNumbers` | array<object> |  |
| `messages.messages[].group.senders` | array<object> |  |
| `messages.messages[].group.tags` | array<string> |  |
| `messages.messages[].group.users` | array<object> |  |
| `messages.messages[].group.useSharedPool` | boolean |  |
| `messages.messages[].id` | string |  |
| `messages.messages[].media` | array<object> | List of media objects attached to message |
| `messages.messages[].media.media[].filename` | string |  |
| `messages.messages[].media.media[].name` | string |  |
| `messages.messages[].media.media[].type` | string |  |
| `messages.messages[].media.media[].url` | string |  |
| `messages.messages[].message` | string |  |
| `messages.messages[].outgoing` | boolean |  |
| `messages.messages[].phoneNumber` | string |  |
| `messages.messages[].price` | number |  |
| `messages.messages[].read` | boolean |  |
| `messages.messages[].segments` | number |  |
| `messages.messages[].sendAt` | date |  |
| `messages.messages[].status` | string |  |
| `messages.messages[].template` | string |  |
| `messages.messages[].type` | string |  |
| `messages.messages[].updated` | object |  |
| `messages.messages[].updated.at` | date |  |
| `messages.messages[].updated.by` | object |  |
| `requested` | number |  |
| `valid` | number |  |

## Native endpoint

Through the native Sakari SMS API, this operation is `POST /v1/accounts/:accountId/messages` (base URL `https://api.sakari.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-messages.md) for the provider-specific parameters and requirements.

