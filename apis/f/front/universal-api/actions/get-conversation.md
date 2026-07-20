# Front: Get Conversation

Retrieves detailed conversation information from Front.

```
GET https://connect.mindcloud.co/v1/universal/front/latest/actions/get-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Front `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/front/latest/actions/get-conversation?connectionId=$CONNECTION_ID&conversationId=cnv_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "conversationId": "cnv_123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/front/latest/actions/get-conversation?${params}`, {
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
| `conversationId` | string | yes | Example: `cnv_123`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignee": {},
      "createdAt": 1,
      "id": "string",
      "isPrivate": true,
      "links": {
        "related": {
          "comments": "https://example.com",
          "events": "https://example.com",
          "followers": "https://example.com",
          "inboxes": "https://example.com",
          "lastMessage": "https://example.com",
          "messages": "https://example.com"
        },
        "self": "https://example.com"
      },
      "recipient": {
        "handle": "string",
        "links": {
          "related": {
            "contact": {}
          }
        },
        "name": {},
        "role": "string"
      },
      "status": "string",
      "statusCategory": "string",
      "statusId": "string",
      "subject": "string",
      "tags": [
        {
          "createdAt": 1,
          "description": {},
          "highlight": {},
          "id": "string",
          "isPrivate": true,
          "isVisibleInConversationLists": true,
          "links": {
            "related": {
              "children": {},
              "conversations": "https://example.com",
              "owner": "https://example.com",
              "parentTag": {}
            },
            "self": "https://example.com"
          },
          "name": "Ava Chen",
          "updatedAt": 1
        }
      ],
      "ticketIds": [
        "string"
      ],
      "updatedAt": 1,
      "waitingSince": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee` | object |  |
| `createdAt` | number |  |
| `id` | string |  |
| `isPrivate` | boolean |  |
| `links.related.comments` | string |  |
| `links.related.events` | string |  |
| `links.related.followers` | string |  |
| `links.related.inboxes` | string |  |
| `links.related.lastMessage` | string |  |
| `links.related.messages` | string |  |
| `links.self` | string |  |
| `recipient.handle` | string |  |
| `recipient.links.related.contact` | object |  |
| `recipient.name` | object |  |
| `recipient.role` | string |  |
| `status` | string |  |
| `statusCategory` | string |  |
| `statusId` | string |  |
| `subject` | string |  |
| `tags[].createdAt` | number |  |
| `tags[].description` | object |  |
| `tags[].highlight` | object |  |
| `tags[].id` | string |  |
| `tags[].isPrivate` | boolean |  |
| `tags[].isVisibleInConversationLists` | boolean |  |
| `tags[].links.related.children` | object |  |
| `tags[].links.related.conversations` | string |  |
| `tags[].links.related.owner` | string |  |
| `tags[].links.related.parentTag` | object |  |
| `tags[].links.self` | string |  |
| `tags[].name` | string |  |
| `tags[].updatedAt` | number |  |
| `ticketIds[]` | string |  |
| `updatedAt` | number |  |
| `waitingSince` | number |  |

## Native endpoint

Through the native Front API, this operation is `GET /conversations/:conversation_id` (base URL `https://api2.frontapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation.md) for the provider-specific parameters and requirements.

