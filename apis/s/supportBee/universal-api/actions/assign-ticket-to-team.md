# SupportBee: Assign Ticket to Team

Assigns a SupportBee ticket to a team.

```
PUT https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/assign-ticket-to-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SupportBee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/assign-ticket-to-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "teamAssignment.teamId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/assign-ticket-to-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "teamAssignment.teamId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | SupportBee ticket ID. |
| `teamAssignment.teamId` | number | yes | SupportBee team ID to assign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "teamAssignment": {
        "assignee": {
          "team": {
            "id": 1,
            "name": "Ava Chen",
            "picture": {
              "thumb128": "string",
              "thumb20": "string",
              "thumb24": "string",
              "thumb256": "string",
              "thumb32": "string",
              "thumb48": "string",
              "thumb64": "string"
            }
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
| `teamAssignment` | object |  |
| `teamAssignment.assignee` | object |  |
| `teamAssignment.assignee.team` | object |  |
| `teamAssignment.assignee.team.id` | number |  |
| `teamAssignment.assignee.team.name` | string |  |
| `teamAssignment.assignee.team.picture` | object |  |
| `teamAssignment.assignee.team.picture.thumb128` | string |  |
| `teamAssignment.assignee.team.picture.thumb20` | string |  |
| `teamAssignment.assignee.team.picture.thumb24` | string |  |
| `teamAssignment.assignee.team.picture.thumb256` | string |  |
| `teamAssignment.assignee.team.picture.thumb32` | string |  |
| `teamAssignment.assignee.team.picture.thumb48` | string |  |
| `teamAssignment.assignee.team.picture.thumb64` | string |  |
| `teamAssignment.createdAt` | string |  |
| `teamAssignment.id` | number |  |
| `teamAssignment.ticket` | object |  |
| `teamAssignment.ticket.id` | number |  |

## Native endpoint

Through the native SupportBee API, this operation is `POST /tickets/:id/team_assignment` (base URL `https://{{credentials.company}}.supportbee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-ticket-to-team.md) for the provider-specific parameters and requirements.

