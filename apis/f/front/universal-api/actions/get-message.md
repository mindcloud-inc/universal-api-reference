# Front: Get Message

Retrieves detailed message information from Front.

```
GET https://connect.mindcloud.co/v1/universal/front/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Front `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/front/latest/actions/get-message?connectionId=$CONNECTION_ID&messageId=msg_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageId": "msg_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/front/latest/actions/get-message?${params}`, {
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
| `messageId` | string | yes | Example: `msg_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {
        "email": "ava@example.com",
        "firstName": "Ava",
        "id": "string",
        "isAdmin": true,
        "isAvailable": true,
        "isBlocked": true,
        "lastName": "Chen",
        "links": {
          "related": {
            "conversations": "https://example.com",
            "inboxes": "https://example.com"
          },
          "self": "https://example.com"
        },
        "type": "string",
        "username": "Ava Chen"
      },
      "blurb": "string",
      "body": "string",
      "createdAt": 1,
      "draftMode": "string",
      "errorType": {},
      "id": "string",
      "isDraft": true,
      "isInbound": true,
      "links": {
        "related": {
          "conversation": "https://example.com",
          "messageRepliedTo": "https://example.com",
          "messageSeen": "https://example.com"
        },
        "self": "https://example.com"
      },
      "messageUid": "string",
      "recipients": [
        {
          "handle": "string",
          "links": {
            "related": {
              "contact": {}
            }
          },
          "name": "Ava Chen",
          "role": "string"
        }
      ],
      "signature": {},
      "subject": "string",
      "text": "string",
      "type": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author.email` | string |  |
| `author.firstName` | string |  |
| `author.id` | string |  |
| `author.isAdmin` | boolean |  |
| `author.isAvailable` | boolean |  |
| `author.isBlocked` | boolean |  |
| `author.lastName` | string |  |
| `author.links.related.conversations` | string |  |
| `author.links.related.inboxes` | string |  |
| `author.links.self` | string |  |
| `author.type` | string |  |
| `author.username` | string |  |
| `blurb` | string |  |
| `body` | string |  |
| `createdAt` | number |  |
| `draftMode` | string |  |
| `errorType` | object |  |
| `id` | string |  |
| `isDraft` | boolean |  |
| `isInbound` | boolean |  |
| `links.related.conversation` | string |  |
| `links.related.messageRepliedTo` | string |  |
| `links.related.messageSeen` | string |  |
| `links.self` | string |  |
| `messageUid` | string |  |
| `recipients[].handle` | string |  |
| `recipients[].links.related.contact` | object |  |
| `recipients[].name` | string |  |
| `recipients[].role` | string |  |
| `signature` | object |  |
| `subject` | string |  |
| `text` | string |  |
| `type` | string |  |
| `version` | string |  |

## Native endpoint

Through the native Front API, this operation is `GET /messages/:message_id` (base URL `https://api2.frontapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

