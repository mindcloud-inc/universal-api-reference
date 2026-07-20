# SupportBee: Create Ticket

Creates a new ticket in SupportBee.

```
POST https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/create-ticket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SupportBee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/create-ticket" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ticket.subject": "string",
  "ticket.requesterEmail": "ava@example.com",
  "ticket.content.text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/create-ticket', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ticket.subject": "string",
    "ticket.requesterEmail": "ava@example.com",
    "ticket.content.text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ticket.subject` | string | yes | Ticket subject line. |
| `ticket.requesterName` | string | no | Requester display name. |
| `ticket.requesterEmail` | string | yes | Requester email address. |
| `ticket.notifyRequester` | boolean | no | Whether to notify the requester on create. |
| `ticket.content.text` | string | yes | Plain-text ticket body. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ticket": {
        "agentRepliesCount": 1,
        "archived": true,
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
        "commentsCount": 1,
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
        "currentTeamAssignee": {},
        "currentUserAssignee": {},
        "customerRating": {},
        "draft": true,
        "historicalImport": {},
        "id": 1,
        "labels": [
          [
            "string"
          ]
        ],
        "lastActivityAt": "string",
        "lastReplyAt": "string",
        "notifyRequester": true,
        "private": true,
        "repliesCount": 1,
        "requester": {
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
        "snoozed": true,
        "snoozedUntil": {},
        "source": {
          "web": "string"
        },
        "spam": true,
        "subject": "string",
        "submitter": {
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
        "trash": true,
        "unanswered": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ticket` | object |  |
| `ticket.agentRepliesCount` | number |  |
| `ticket.archived` | boolean |  |
| `ticket.attachmentsCount` | number |  |
| `ticket.bcc[]` | array |  |
| `ticket.cc[]` | array |  |
| `ticket.commentsCount` | number |  |
| `ticket.content` | object |  |
| `ticket.content.attachments[]` | array |  |
| `ticket.content.html` | string |  |
| `ticket.content.text` | string |  |
| `ticket.content.truncated` | boolean |  |
| `ticket.createdAt` | string |  |
| `ticket.currentTeamAssignee` | object |  |
| `ticket.currentUserAssignee` | object |  |
| `ticket.customerRating` | object |  |
| `ticket.draft` | boolean |  |
| `ticket.historicalImport` | object |  |
| `ticket.id` | number |  |
| `ticket.labels[]` | array |  |
| `ticket.lastActivityAt` | string |  |
| `ticket.lastReplyAt` | string |  |
| `ticket.notifyRequester` | boolean |  |
| `ticket.private` | boolean |  |
| `ticket.repliesCount` | number |  |
| `ticket.requester` | object |  |
| `ticket.requester.agent` | boolean |  |
| `ticket.requester.canMembersAccessGroupTickets` | object |  |
| `ticket.requester.email` | string |  |
| `ticket.requester.emailDomains[]` | array |  |
| `ticket.requester.firstName` | string |  |
| `ticket.requester.id` | number |  |
| `ticket.requester.lastName` | string |  |
| `ticket.requester.membersCount` | number |  |
| `ticket.requester.name` | string |  |
| `ticket.requester.picture` | object |  |
| `ticket.requester.picture.thumb128` | string |  |
| `ticket.requester.picture.thumb20` | string |  |
| `ticket.requester.picture.thumb24` | string |  |
| `ticket.requester.picture.thumb32` | string |  |
| `ticket.requester.picture.thumb48` | string |  |
| `ticket.requester.picture.thumb64` | string |  |
| `ticket.requester.role` | string |  |
| `ticket.requester.twoFactorAuthenticationEnabled` | boolean |  |
| `ticket.requester.type` | string |  |
| `ticket.snoozed` | boolean |  |
| `ticket.snoozedUntil` | object |  |
| `ticket.source` | object |  |
| `ticket.source.web` | string |  |
| `ticket.spam` | boolean |  |
| `ticket.subject` | string |  |
| `ticket.submitter` | object |  |
| `ticket.submitter.agent` | boolean |  |
| `ticket.submitter.canMembersAccessGroupTickets` | object |  |
| `ticket.submitter.email` | string |  |
| `ticket.submitter.emailDomains[]` | array |  |
| `ticket.submitter.firstName` | string |  |
| `ticket.submitter.id` | number |  |
| `ticket.submitter.lastName` | string |  |
| `ticket.submitter.membersCount` | number |  |
| `ticket.submitter.name` | string |  |
| `ticket.submitter.picture` | object |  |
| `ticket.submitter.picture.thumb128` | string |  |
| `ticket.submitter.picture.thumb20` | string |  |
| `ticket.submitter.picture.thumb24` | string |  |
| `ticket.submitter.picture.thumb32` | string |  |
| `ticket.submitter.picture.thumb48` | string |  |
| `ticket.submitter.picture.thumb64` | string |  |
| `ticket.submitter.role` | string |  |
| `ticket.submitter.twoFactorAuthenticationEnabled` | boolean |  |
| `ticket.submitter.type` | string |  |
| `ticket.summary` | string |  |
| `ticket.trash` | boolean |  |
| `ticket.unanswered` | boolean |  |

## Native endpoint

Through the native SupportBee API, this operation is `POST /tickets` (base URL `https://{{credentials.company}}.supportbee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket.md) for the provider-specific parameters and requirements.

