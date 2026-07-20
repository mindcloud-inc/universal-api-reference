# SupportBee: List Ticket Replies

Retrieves replies for a SupportBee ticket.

```
GET https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/list-ticket-replies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SupportBee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/list-ticket-replies?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/list-ticket-replies?${params}`, {
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
      "replies": [
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
| `replies[]` | array<object> |  |
| `replies[].attachmentsCount` | number |  |
| `replies[].bcc[]` | array |  |
| `replies[].cc[]` | array |  |
| `replies[].content` | object |  |
| `replies[].content.attachments[]` | array |  |
| `replies[].content.html` | string |  |
| `replies[].content.text` | string |  |
| `replies[].content.truncated` | boolean |  |
| `replies[].createdAt` | string |  |
| `replies[].historicalImport` | object |  |
| `replies[].id` | number |  |
| `replies[].merged` | boolean |  |
| `replies[].replier` | object |  |
| `replies[].replier.agent` | boolean |  |
| `replies[].replier.canMembersAccessGroupTickets` | object |  |
| `replies[].replier.email` | string |  |
| `replies[].replier.emailDomains[]` | array |  |
| `replies[].replier.firstName` | string |  |
| `replies[].replier.id` | number |  |
| `replies[].replier.lastName` | string |  |
| `replies[].replier.membersCount` | number |  |
| `replies[].replier.name` | string |  |
| `replies[].replier.picture` | object |  |
| `replies[].replier.picture.thumb128` | string |  |
| `replies[].replier.picture.thumb20` | string |  |
| `replies[].replier.picture.thumb24` | string |  |
| `replies[].replier.picture.thumb32` | string |  |
| `replies[].replier.picture.thumb48` | string |  |
| `replies[].replier.picture.thumb64` | string |  |
| `replies[].replier.role` | string |  |
| `replies[].replier.twoFactorAuthenticationEnabled` | boolean |  |
| `replies[].replier.type` | string |  |
| `replies[].summary` | string |  |
| `replies[].ticket` | object |  |
| `replies[].ticket.agentRepliesCount` | number |  |
| `replies[].ticket.commentsCount` | number |  |
| `replies[].ticket.id` | number |  |
| `replies[].ticket.repliesCount` | number |  |

## Native endpoint

Through the native SupportBee API, this operation is `GET /tickets/:id/replies` (base URL `https://{{credentials.company}}.supportbee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ticket-replies.md) for the provider-specific parameters and requirements.

