# SupportBee: Search Tickets

Finds tickets in SupportBee by search query.

```
GET https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/search-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SupportBee `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/search-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/search-tickets?${params}`, {
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
| `query` | string | yes | Search query string. |
| `spam` | boolean | no | If true, include spam tickets. |
| `trash` | boolean | no | If true, include trashed tickets. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currentPage": 1,
      "perPage": 1,
      "tickets": [
        [
          {}
        ]
      ],
      "total": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currentPage` | number |  |
| `perPage` | number |  |
| `tickets[]` | array<object> |  |
| `tickets[].agentRepliesCount` | number |  |
| `tickets[].archived` | boolean |  |
| `tickets[].attachmentsCount` | number |  |
| `tickets[].bcc[]` | array |  |
| `tickets[].cc[]` | array |  |
| `tickets[].commentsCount` | number |  |
| `tickets[].content` | object |  |
| `tickets[].content.attachments[]` | array |  |
| `tickets[].content.html` | string |  |
| `tickets[].content.text` | string |  |
| `tickets[].content.truncated` | boolean |  |
| `tickets[].createdAt` | string |  |
| `tickets[].currentTeamAssignee` | object |  |
| `tickets[].currentUserAssignee` | object |  |
| `tickets[].customerRating` | object |  |
| `tickets[].draft` | boolean |  |
| `tickets[].historicalImport` | object |  |
| `tickets[].id` | number |  |
| `tickets[].labels[]` | array |  |
| `tickets[].lastActivityAt` | string |  |
| `tickets[].lastReplyAt` | string |  |
| `tickets[].notifyRequester` | boolean |  |
| `tickets[].private` | boolean |  |
| `tickets[].repliesCount` | number |  |
| `tickets[].requester` | object |  |
| `tickets[].requester.agent` | boolean |  |
| `tickets[].requester.canMembersAccessGroupTickets` | object |  |
| `tickets[].requester.email` | string |  |
| `tickets[].requester.emailDomains[]` | array |  |
| `tickets[].requester.firstName` | string |  |
| `tickets[].requester.id` | number |  |
| `tickets[].requester.lastName` | object |  |
| `tickets[].requester.membersCount` | number |  |
| `tickets[].requester.name` | string |  |
| `tickets[].requester.picture` | object |  |
| `tickets[].requester.picture.thumb128` | string |  |
| `tickets[].requester.picture.thumb20` | string |  |
| `tickets[].requester.picture.thumb24` | string |  |
| `tickets[].requester.picture.thumb32` | string |  |
| `tickets[].requester.picture.thumb48` | string |  |
| `tickets[].requester.picture.thumb64` | string |  |
| `tickets[].requester.role` | string |  |
| `tickets[].requester.twoFactorAuthenticationEnabled` | boolean |  |
| `tickets[].requester.type` | string |  |
| `tickets[].snoozed` | boolean |  |
| `tickets[].snoozedUntil` | object |  |
| `tickets[].source` | object |  |
| `tickets[].source.web` | string |  |
| `tickets[].spam` | boolean |  |
| `tickets[].subject` | string |  |
| `tickets[].submitter` | object |  |
| `tickets[].submitter.agent` | boolean |  |
| `tickets[].submitter.canMembersAccessGroupTickets` | object |  |
| `tickets[].submitter.email` | string |  |
| `tickets[].submitter.emailDomains[]` | array |  |
| `tickets[].submitter.firstName` | string |  |
| `tickets[].submitter.id` | number |  |
| `tickets[].submitter.lastName` | object |  |
| `tickets[].submitter.membersCount` | number |  |
| `tickets[].submitter.name` | string |  |
| `tickets[].submitter.picture` | object |  |
| `tickets[].submitter.picture.thumb128` | string |  |
| `tickets[].submitter.picture.thumb20` | string |  |
| `tickets[].submitter.picture.thumb24` | string |  |
| `tickets[].submitter.picture.thumb32` | string |  |
| `tickets[].submitter.picture.thumb48` | string |  |
| `tickets[].submitter.picture.thumb64` | string |  |
| `tickets[].submitter.role` | string |  |
| `tickets[].submitter.twoFactorAuthenticationEnabled` | boolean |  |
| `tickets[].submitter.type` | string |  |
| `tickets[].summary` | string |  |
| `tickets[].trash` | boolean |  |
| `tickets[].unanswered` | boolean |  |
| `total` | number |  |
| `totalPages` | number |  |

## Native endpoint

Through the native SupportBee API, this operation is `GET /tickets/search` (base URL `https://{{credentials.company}}.supportbee.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-tickets.md) for the provider-specific parameters and requirements.

