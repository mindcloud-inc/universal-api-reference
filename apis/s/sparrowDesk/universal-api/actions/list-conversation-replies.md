# SparrowDesk: List Conversation Replies

Retrieves conversation replies from SparrowDesk.

```
GET https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/list-conversation-replies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SparrowDesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/list-conversation-replies?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sparrowDesk/latest/actions/list-conversation-replies?${params}`, {
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
| `id` | number | yes | SparrowDesk conversation ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "attachments": [
        {}
      ],
      "author": {
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen",
        "phone": "string",
        "type": "string"
      },
      "bodyHtml": "string",
      "bodyText": "string",
      "brandId": 1,
      "conversationId": 1,
      "id": "string",
      "pages": {
        "perPage": 1
      },
      "sentAt": 1,
      "totalCount": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number | Account ID. |
| `attachments` | array<object> | Reply attachments. |
| `author.email` | string | Author email. |
| `author.id` | number | Author ID. |
| `author.name` | string | Author name. |
| `author.phone` | string | Author phone number. |
| `author.type` | string | Author type. |
| `bodyHtml` | string | HTML body. |
| `bodyText` | string | Plain-text body. |
| `brandId` | number | Brand ID. |
| `conversationId` | number | Conversation ID. |
| `id` | string | Reply ID. |
| `pages.perPage` | number | Page size. |
| `sentAt` | number | Sent timestamp. |
| `totalCount` | number | Total number of replies. |
| `type` | string | Reply type. |

## Native endpoint

Through the native SparrowDesk API, this operation is `GET /conversations/{{id}}/replies` (base URL `https://api.sparrowdesk.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversation-replies.md) for the provider-specific parameters and requirements.

