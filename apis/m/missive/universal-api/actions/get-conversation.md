# Missive: Get Conversation

Retrieves a conversation from your Missive workspace.

```
GET https://connect.mindcloud.co/v1/universal/missive/latest/actions/get-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Missive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/missive/latest/actions/get-conversation?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/missive/latest/actions/get-conversation?${params}`, {
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
| `id` | string | yes | Conversation ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appUrl": "https://example.com",
      "assigneeEmails": "ava@example.com",
      "assigneeNames": "Ava Chen",
      "attachmentsCount": 1,
      "closedAt": {},
      "color": {},
      "completedTasksCount": 1,
      "createdAt": 1,
      "draftsCount": 1,
      "id": "string",
      "lastActivityAt": 1,
      "latestMessageSubject": {},
      "messagesCount": 1,
      "organization": {},
      "sendLaterMessagesCount": 1,
      "sharedLabelNames": "Ava Chen",
      "subject": {},
      "tasksCount": 1,
      "team": {},
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appUrl` | string |  |
| `assigneeEmails` | string |  |
| `assigneeNames` | string |  |
| `attachmentsCount` | number |  |
| `closedAt` | object |  |
| `color` | object |  |
| `completedTasksCount` | number |  |
| `createdAt` | number |  |
| `draftsCount` | number |  |
| `id` | string |  |
| `lastActivityAt` | number |  |
| `latestMessageSubject` | object |  |
| `messagesCount` | number |  |
| `organization` | object |  |
| `sendLaterMessagesCount` | number |  |
| `sharedLabelNames` | string |  |
| `subject` | object |  |
| `tasksCount` | number |  |
| `team` | object |  |
| `users[].archived` | boolean |  |
| `users[].assigned` | boolean |  |
| `users[].closed` | boolean |  |
| `users[].email` | string |  |
| `users[].flagged` | boolean |  |
| `users[].id` | string |  |
| `users[].junked` | boolean |  |
| `users[].name` | string |  |
| `users[].snoozed` | boolean |  |
| `users[].trashed` | boolean |  |
| `users[].unassigned` | boolean |  |
| `webUrl` | string |  |

## Native endpoint

Through the native Missive API, this operation is `GET /conversations/:id` (base URL `https://public.missiveapp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation.md) for the provider-specific parameters and requirements.

