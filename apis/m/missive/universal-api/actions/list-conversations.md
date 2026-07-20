# Missive: List Conversations

Retrieves conversations from your Missive workspace.

```
GET https://connect.mindcloud.co/v1/universal/missive/latest/actions/list-conversations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Missive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/missive/latest/actions/list-conversations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/missive/latest/actions/list-conversations?${params}`, {
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
| `limit` | number | no | Number of conversations returned. Default 25, max 50. |
| `until` | number | no | Unix timestamp used to paginate with the oldest conversation last_activity_at value from the previous page. |
| `inbox` | boolean | no | Pass true to list conversations in the Inbox mailbox. |
| `all` | boolean | no | Pass true to list conversations in the All mailbox. |
| `assigned` | boolean | no | Pass true to list conversations assigned to the token owner. |
| `closed` | boolean | no | Pass true to list conversations in Closed. |
| `snoozed` | boolean | no | Pass true to list conversations in Snoozed. |
| `flagged` | boolean | no | Pass true to list conversations in Starred. |
| `trashed` | boolean | no | Pass true to list conversations in Trash. |
| `junked` | boolean | no | Pass true to list conversations in Spam. |
| `drafts` | boolean | no | Pass true to list conversations in Drafts. |
| `sharedLabel` | string | no | Shared label ID to filter conversations in that shared label. |
| `teamInbox` | string | no | Team ID to list conversations in the team's Inbox mailbox. |
| `teamClosed` | string | no | Team ID to list conversations in the team's Closed mailbox. |
| `teamAll` | string | no | Team ID to list conversations in the team's All mailbox. |
| `organization` | string | no | Organization ID to restrict conversations shared with the organization. |
| `email` | string | no | Specific contact email address filter. Mutually exclusive with Domain and Contact Organization. |
| `domain` | string | no | Specific contact email domain filter. Mutually exclusive with Email and Contact Organization. |
| `contactOrganization` | string | no | Contact organization or group UUID filter. Mutually exclusive with Email and Domain. |

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
      "organization": {
        "id": "string",
        "name": "Ava Chen"
      },
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
| `organization.id` | string |  |
| `organization.name` | string |  |
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

Through the native Missive API, this operation is `GET /conversations` (base URL `https://public.missiveapp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-conversations.md) for the provider-specific parameters and requirements.

