# Missive: Get Message

Retrieves a message from your Missive workspace.

```
GET https://connect.mindcloud.co/v1/universal/missive/latest/actions/get-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Missive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/missive/latest/actions/get-message?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/missive/latest/actions/get-message?${params}`, {
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
| `id` | string | yes | Message ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {},
      "body": "string",
      "conversation": {
        "appUrl": "https://example.com",
        "assigneeEmails": "ava@example.com",
        "assigneeNames": "Ava Chen",
        "attachmentsCount": 1,
        "authors": [
          {
            "name": "Ava Chen"
          }
        ],
        "closedAt": {},
        "color": {},
        "completedTasksCount": 1,
        "createdAt": 1,
        "draftsCount": 1,
        "externalAuthors": [
          {
            "name": "Ava Chen"
          }
        ],
        "id": "string",
        "latestMessageSubject": "string",
        "messagesCount": 1,
        "organization": {
          "id": "string",
          "name": "Ava Chen"
        },
        "sendLaterMessagesCount": 1,
        "sharedLabelNames": "Ava Chen",
        "subject": {},
        "tasksCount": 1,
        "team": {
          "id": "string",
          "name": "Ava Chen",
          "observers": [
            "string"
          ],
          "organization": "string"
        },
        "users": [
          {
            "archived": true,
            "assigned": true,
            "closed": true,
            "email": "ava@example.com",
            "flagged": true,
            "id": "string",
            "junked": true,
            "name": "Ava Chen",
            "snoozed": true,
            "trashed": true,
            "unassigned": true
          }
        ],
        "webUrl": "https://example.com"
      },
      "createdAt": 1,
      "deliveredAt": 1,
      "externalId": {},
      "fromField": {
        "id": "string",
        "name": "Ava Chen",
        "username": "Ava Chen"
      },
      "id": "string",
      "preview": "string",
      "toFields": [
        {
          "id": "string",
          "name": "Ava Chen",
          "username": "Ava Chen"
        }
      ],
      "type": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | object |  |
| `body` | string |  |
| `conversation.appUrl` | string |  |
| `conversation.assigneeEmails` | string |  |
| `conversation.assigneeNames` | string |  |
| `conversation.attachmentsCount` | number |  |
| `conversation.authors[].name` | string |  |
| `conversation.closedAt` | object |  |
| `conversation.color` | object |  |
| `conversation.completedTasksCount` | number |  |
| `conversation.createdAt` | number |  |
| `conversation.draftsCount` | number |  |
| `conversation.externalAuthors[].name` | string |  |
| `conversation.id` | string |  |
| `conversation.latestMessageSubject` | string |  |
| `conversation.messagesCount` | number |  |
| `conversation.organization.id` | string |  |
| `conversation.organization.name` | string |  |
| `conversation.sendLaterMessagesCount` | number |  |
| `conversation.sharedLabelNames` | string |  |
| `conversation.subject` | object |  |
| `conversation.tasksCount` | number |  |
| `conversation.team.id` | string |  |
| `conversation.team.name` | string |  |
| `conversation.team.observers[]` | string |  |
| `conversation.team.organization` | string |  |
| `conversation.users[].archived` | boolean |  |
| `conversation.users[].assigned` | boolean |  |
| `conversation.users[].closed` | boolean |  |
| `conversation.users[].email` | string |  |
| `conversation.users[].flagged` | boolean |  |
| `conversation.users[].id` | string |  |
| `conversation.users[].junked` | boolean |  |
| `conversation.users[].name` | string |  |
| `conversation.users[].snoozed` | boolean |  |
| `conversation.users[].trashed` | boolean |  |
| `conversation.users[].unassigned` | boolean |  |
| `conversation.webUrl` | string |  |
| `createdAt` | number |  |
| `deliveredAt` | number |  |
| `externalId` | object |  |
| `fromField.id` | string |  |
| `fromField.name` | string |  |
| `fromField.username` | string |  |
| `id` | string |  |
| `preview` | string |  |
| `toFields[].id` | string |  |
| `toFields[].name` | string |  |
| `toFields[].username` | string |  |
| `type` | string |  |
| `updatedAt` | number |  |

## Native endpoint

Through the native Missive API, this operation is `GET /messages/:id` (base URL `https://public.missiveapp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-message.md) for the provider-specific parameters and requirements.

