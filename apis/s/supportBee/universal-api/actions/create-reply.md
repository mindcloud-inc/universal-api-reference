# SupportBee: Create Reply

Creates a reply on a SupportBee ticket.

```
POST https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/create-reply
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SupportBee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/create-reply" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "reply.content.text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/create-reply', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "reply.content.text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | SupportBee ticket ID. |
| `reply.content.text` | string | yes | Plain-text reply body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "reply": {
        "attachmentsCount": 1,
        "bcc": [
          [
            "string"
          ]
        ],
        "cc": [
          [
            "string"
          ]
        ],
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
        "historicalImport": {},
        "id": 1,
        "merged": true,
        "replier": {
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
        "summary": "string",
        "ticket": {
          "agentRepliesCount": 1,
          "commentsCount": 1,
          "id": 1,
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
| `reply` | object |  |
| `reply.attachmentsCount` | number |  |
| `reply.bcc[]` | array |  |
| `reply.cc[]` | array |  |
| `reply.content` | object |  |
| `reply.content.attachments[]` | array |  |
| `reply.content.html` | string |  |
| `reply.content.text` | string |  |
| `reply.content.truncated` | boolean |  |
| `reply.createdAt` | string |  |
| `reply.historicalImport` | object |  |
| `reply.id` | number |  |
| `reply.merged` | boolean |  |
| `reply.replier` | object |  |
| `reply.replier.agent` | boolean |  |
| `reply.replier.canMembersAccessGroupTickets` | object |  |
| `reply.replier.email` | string |  |
| `reply.replier.emailDomains[]` | array |  |
| `reply.replier.firstName` | string |  |
| `reply.replier.id` | number |  |
| `reply.replier.lastName` | string |  |
| `reply.replier.membersCount` | number |  |
| `reply.replier.name` | string |  |
| `reply.replier.picture` | object |  |
| `reply.replier.picture.thumb128` | string |  |
| `reply.replier.picture.thumb20` | string |  |
| `reply.replier.picture.thumb24` | string |  |
| `reply.replier.picture.thumb32` | string |  |
| `reply.replier.picture.thumb48` | string |  |
| `reply.replier.picture.thumb64` | string |  |
| `reply.replier.role` | string |  |
| `reply.replier.twoFactorAuthenticationEnabled` | boolean |  |
| `reply.replier.type` | string |  |
| `reply.summary` | string |  |
| `reply.ticket` | object |  |
| `reply.ticket.agentRepliesCount` | number |  |
| `reply.ticket.commentsCount` | number |  |
| `reply.ticket.id` | number |  |
| `reply.ticket.repliesCount` | number |  |

## Native endpoint

Through the native SupportBee API, this operation is `POST /tickets/:id/replies` (base URL `https://{{credentials.company}}.supportbee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-reply.md) for the provider-specific parameters and requirements.

