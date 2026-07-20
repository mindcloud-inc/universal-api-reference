# SupportBee: Create Comment

Creates a comment on a SupportBee ticket.

```
POST https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/create-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SupportBee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "comment.content.text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "comment.content.text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | SupportBee ticket ID. |
| `comment.content.text` | string | yes | Plain-text internal comment body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comment": {
        "commenter": {
          "agent": true,
          "canMembersAccessGroupTickets": {},
          "email": "ava@example.com",
          "emailDomains": [
            [
              "ava@example.com"
            ]
          ],
          "firstName": "Ava",
          "id": 1,
          "lastName": "Chen",
          "membersCount": 1,
          "name": "Ava Chen",
          "picture": {
            "thumb128": "string",
            "thumb20": "string",
            "thumb24": "string",
            "thumb32": "string",
            "thumb48": "string",
            "thumb64": "string"
          },
          "role": "string",
          "twoFactorAuthenticationEnabled": true,
          "type": "string"
        },
        "content": {
          "attachments": [
            [
              "string"
            ]
          ],
          "html": "string",
          "text": "string",
          "truncated": true
        },
        "createdAt": "string",
        "id": 1,
        "merged": true,
        "ticket": {
          "agentRepliesCount": 1,
          "commentsCount": 1,
          "repliesCount": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `comment` | object |  |
| `comment.commenter` | object |  |
| `comment.commenter.agent` | boolean |  |
| `comment.commenter.canMembersAccessGroupTickets` | object |  |
| `comment.commenter.email` | string |  |
| `comment.commenter.emailDomains[]` | array |  |
| `comment.commenter.firstName` | string |  |
| `comment.commenter.id` | number |  |
| `comment.commenter.lastName` | string |  |
| `comment.commenter.membersCount` | number |  |
| `comment.commenter.name` | string |  |
| `comment.commenter.picture` | object |  |
| `comment.commenter.picture.thumb128` | string |  |
| `comment.commenter.picture.thumb20` | string |  |
| `comment.commenter.picture.thumb24` | string |  |
| `comment.commenter.picture.thumb32` | string |  |
| `comment.commenter.picture.thumb48` | string |  |
| `comment.commenter.picture.thumb64` | string |  |
| `comment.commenter.role` | string |  |
| `comment.commenter.twoFactorAuthenticationEnabled` | boolean |  |
| `comment.commenter.type` | string |  |
| `comment.content` | object |  |
| `comment.content.attachments[]` | array |  |
| `comment.content.html` | string |  |
| `comment.content.text` | string |  |
| `comment.content.truncated` | boolean |  |
| `comment.createdAt` | string |  |
| `comment.id` | number |  |
| `comment.merged` | boolean |  |
| `comment.ticket` | object |  |
| `comment.ticket.agentRepliesCount` | number |  |
| `comment.ticket.commentsCount` | number |  |
| `comment.ticket.repliesCount` | number |  |

## Native endpoint

Through the native SupportBee API, this operation is `POST /tickets/:id/comments` (base URL `https://{{credentials.company}}.supportbee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-comment.md) for the provider-specific parameters and requirements.

