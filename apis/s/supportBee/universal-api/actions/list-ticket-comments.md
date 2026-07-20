# SupportBee: List Ticket Comments

Retrieves comments for a SupportBee ticket.

```
GET https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/list-ticket-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SupportBee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/list-ticket-comments?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/list-ticket-comments?${params}`, {
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
| `id` | number | yes | SupportBee ticket ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comments[]` | array<object> |  |
| `comments[].commenter` | object |  |
| `comments[].commenter.agent` | boolean |  |
| `comments[].commenter.canMembersAccessGroupTickets` | object |  |
| `comments[].commenter.email` | string |  |
| `comments[].commenter.emailDomains[]` | array |  |
| `comments[].commenter.firstName` | string |  |
| `comments[].commenter.id` | number |  |
| `comments[].commenter.lastName` | string |  |
| `comments[].commenter.membersCount` | number |  |
| `comments[].commenter.name` | string |  |
| `comments[].commenter.picture` | object |  |
| `comments[].commenter.picture.thumb128` | string |  |
| `comments[].commenter.picture.thumb20` | string |  |
| `comments[].commenter.picture.thumb24` | string |  |
| `comments[].commenter.picture.thumb32` | string |  |
| `comments[].commenter.picture.thumb48` | string |  |
| `comments[].commenter.picture.thumb64` | string |  |
| `comments[].commenter.role` | string |  |
| `comments[].commenter.twoFactorAuthenticationEnabled` | boolean |  |
| `comments[].commenter.type` | string |  |
| `comments[].content` | object |  |
| `comments[].content.attachments[]` | array |  |
| `comments[].content.html` | string |  |
| `comments[].content.text` | string |  |
| `comments[].content.truncated` | boolean |  |
| `comments[].createdAt` | string |  |
| `comments[].id` | number |  |
| `comments[].merged` | boolean |  |
| `comments[].ticket` | object |  |
| `comments[].ticket.agentRepliesCount` | number |  |
| `comments[].ticket.commentsCount` | number |  |
| `comments[].ticket.repliesCount` | number |  |

## Native endpoint

Through the native SupportBee API, this operation is `GET /tickets/:id/comments` (base URL `https://{{credentials.company}}.supportbee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ticket-comments.md) for the provider-specific parameters and requirements.

