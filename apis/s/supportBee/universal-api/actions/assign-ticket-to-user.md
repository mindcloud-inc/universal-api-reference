# SupportBee: Assign Ticket to User

Assigns a SupportBee ticket to a user.

```
PUT https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/assign-ticket-to-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SupportBee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/assign-ticket-to-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "userAssignment.userId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/assign-ticket-to-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "userAssignment.userId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | SupportBee ticket ID. |
| `userAssignment.userId` | number | yes | SupportBee user ID to assign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "userAssignment": {
        "assignee": {
          "user": {
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
          }
        },
        "createdAt": "string",
        "id": 1,
        "ticket": {
          "id": 1
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
| `userAssignment` | object |  |
| `userAssignment.assignee` | object |  |
| `userAssignment.assignee.user` | object |  |
| `userAssignment.assignee.user.agent` | boolean |  |
| `userAssignment.assignee.user.canMembersAccessGroupTickets` | object |  |
| `userAssignment.assignee.user.email` | string |  |
| `userAssignment.assignee.user.emailDomains[]` | array |  |
| `userAssignment.assignee.user.firstName` | string |  |
| `userAssignment.assignee.user.id` | number |  |
| `userAssignment.assignee.user.lastName` | string |  |
| `userAssignment.assignee.user.membersCount` | number |  |
| `userAssignment.assignee.user.name` | string |  |
| `userAssignment.assignee.user.picture` | object |  |
| `userAssignment.assignee.user.picture.thumb128` | string |  |
| `userAssignment.assignee.user.picture.thumb20` | string |  |
| `userAssignment.assignee.user.picture.thumb24` | string |  |
| `userAssignment.assignee.user.picture.thumb32` | string |  |
| `userAssignment.assignee.user.picture.thumb48` | string |  |
| `userAssignment.assignee.user.picture.thumb64` | string |  |
| `userAssignment.assignee.user.role` | string |  |
| `userAssignment.assignee.user.twoFactorAuthenticationEnabled` | boolean |  |
| `userAssignment.assignee.user.type` | string |  |
| `userAssignment.createdAt` | string |  |
| `userAssignment.id` | number |  |
| `userAssignment.ticket` | object |  |
| `userAssignment.ticket.id` | number |  |

## Native endpoint

Through the native SupportBee API, this operation is `POST /tickets/:id/user_assignment` (base URL `https://{{credentials.company}}.supportbee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-ticket-to-user.md) for the provider-specific parameters and requirements.

