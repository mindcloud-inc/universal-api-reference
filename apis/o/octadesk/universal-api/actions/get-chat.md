# Octadesk: Get Chat

Retrieves a chat from Octadesk by ID.

```
GET https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/get-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Octadesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/get-chat?connectionId=$CONNECTION_ID&id=07706fb7-54dd-4eb7-88b6-5b8a7bdc1a3e" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "07706fb7-54dd-4eb7-88b6-5b8a7bdc1a3e"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/get-chat?${params}`, {
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
| `id` | string | yes | Chat ID from Octadesk. Example: `07706fb7-54dd-4eb7-88b6-5b8a7bdc1a3e`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "botName": {},
      "channel": "string",
      "contact": {
        "customFields": {},
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen"
      },
      "conversationOrigin": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": [
        "string"
      ],
      "firstMessageDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastMessageDate": "2026-05-07T12:00:00.000Z",
      "messages": [
        {
          "body": "string",
          "chatId": "string",
          "id": "string",
          "readAt": "2026-05-07T12:00:00.000Z",
          "sentBy": {
            "email": "ava@example.com",
            "id": "string",
            "name": "Ava Chen",
            "type": "string"
          },
          "status": "string",
          "time": "2026-05-07T12:00:00.000Z",
          "type": "string"
        }
      ],
      "messagesCount": 1,
      "number": 1,
      "page": 1,
      "pages": 1,
      "pastAgents": [
        "string"
      ],
      "status": "string",
      "survey": {
        "comment": "string",
        "response": "string"
      },
      "tags": [
        "string"
      ],
      "unreadMessages": true,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "waitingTime": {},
      "withBot": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `botName` | object |  |
| `channel` | string |  |
| `contact.customFields` | object |  |
| `contact.email` | string |  |
| `contact.id` | string |  |
| `contact.name` | string |  |
| `conversationOrigin` | object |  |
| `createdAt` | date |  |
| `customFields` | array |  |
| `firstMessageDate` | date |  |
| `id` | string |  |
| `lastMessageDate` | date |  |
| `messages[].body` | string |  |
| `messages[].chatId` | string |  |
| `messages[].id` | string |  |
| `messages[].readAt` | date |  |
| `messages[].sentBy.email` | string |  |
| `messages[].sentBy.id` | string |  |
| `messages[].sentBy.name` | string |  |
| `messages[].sentBy.type` | string |  |
| `messages[].status` | string |  |
| `messages[].time` | date |  |
| `messages[].type` | string |  |
| `messagesCount` | number |  |
| `number` | number |  |
| `page` | number |  |
| `pages` | number |  |
| `pastAgents` | array |  |
| `status` | string |  |
| `survey.comment` | string |  |
| `survey.response` | string |  |
| `tags` | array |  |
| `unreadMessages` | boolean |  |
| `updatedAt` | date |  |
| `waitingTime` | object |  |
| `withBot` | boolean |  |

## Native endpoint

Through the native Octadesk API, this operation is `GET /chat/:id` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chat.md) for the provider-specific parameters and requirements.

