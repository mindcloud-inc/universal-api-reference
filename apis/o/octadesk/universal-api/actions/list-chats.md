# Octadesk: List Chats

Retrieves chats from Octadesk.

```
GET https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/list-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Octadesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/list-chats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/list-chats?${params}`, {
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
| `limit` | string | no | Limit of items per page. MAX = 100, MIN = 1. |
| `page` | string | no | Number of the page. Defaults to 1. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bot": {},
      "botName": {},
      "channel": "string",
      "contact": {
        "customFields": [
          "string"
        ],
        "email": "ava@example.com",
        "id": "string",
        "name": "Ava Chen",
        "organization": {
          "name": "Ava Chen"
        },
        "phoneContacts": [
          "string"
        ]
      },
      "conversationOrigin": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastMessageDate": "2026-05-07T12:00:00.000Z",
      "number": 1,
      "origin": "string",
      "status": "string",
      "statusDetail": "string",
      "survey": {
        "comment": "string",
        "response": "string"
      },
      "tags": [
        "string"
      ],
      "unreadMessages": true,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "withBot": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bot` | object |  |
| `botName` | object |  |
| `channel` | string |  |
| `contact.customFields` | array |  |
| `contact.email` | string |  |
| `contact.id` | string |  |
| `contact.name` | string |  |
| `contact.organization.name` | string |  |
| `contact.phoneContacts` | array |  |
| `conversationOrigin` | object |  |
| `createdAt` | date |  |
| `id` | string |  |
| `lastMessageDate` | date |  |
| `number` | number |  |
| `origin` | string |  |
| `status` | string |  |
| `statusDetail` | string |  |
| `survey.comment` | string |  |
| `survey.response` | string |  |
| `tags` | array |  |
| `unreadMessages` | boolean |  |
| `updatedAt` | date |  |
| `withBot` | boolean |  |

## Native endpoint

Through the native Octadesk API, this operation is `GET /chat` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chats.md) for the provider-specific parameters and requirements.

